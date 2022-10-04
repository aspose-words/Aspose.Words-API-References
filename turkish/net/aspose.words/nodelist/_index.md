---
title: NodeList
second_title: Aspose.Words for .NET API Referansı
description: kullanılarak yürütülen bir XPath sorgusuyla eşleşen düğümler koleksiyonunu temsil eder.SelectNodes./compositenode/selectnodes/ yöntem.
type: docs
weight: 3980
url: /tr/net/aspose.words/nodelist/
---
## NodeList class

kullanılarak yürütülen bir XPath sorgusuyla eşleşen düğümler koleksiyonunu temsil eder.[`SelectNodes`](../compositenode/selectnodes/) yöntem.

```csharp
public class NodeList : IEnumerable<Node>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/nodelist/count/) { get; } | Listedeki düğüm sayısını alır. |
| [Item](../../aspose.words/nodelist/item/) { get; } | Verilen dizindeki bir düğümü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetEnumerator](../../aspose.words/nodelist/getenumerator/)() | Düğüm koleksiyonu üzerinde basit bir "foreach" stili yineleme sağlar. |
| [ToArray](../../aspose.words/nodelist/toarray/)() | Koleksiyondaki tüm düğümleri yeni bir düğüm dizisine kopyalar. |

### Notlar

**Düğüm Listesi** tarafından iade edilir[`SelectNodes`](../compositenode/selectnodes/) ve XPath sorgusuyla eşleşen bir collection düğüm içerir.

**Düğüm Listesi** dizine alınmış erişimi ve yinelemeyi destekler.

tedavi et **Düğüm Listesi** "anlık görüntü" koleksiyonu olarak koleksiyon. **Düğüm Listesi**Start , XPath sorgusu çalıştırıldığında düğümler gerçekten alınmadığından, "canlı" bir koleksiyon olarak başlar. Düğümler yalnızca erişim üzerine alınır ve şu anda düğüm ve 'den önceki tüm düğümler bir "anlık görüntü" koleksiyonu oluşturacak şekilde önbelleğe alınır.

### Örnekler

Bir Word belgesindeki tüm köprülerin nasıl bulunacağını ve ardından bunların URL'lerinin ve görünen adlarının nasıl değiştirileceğini gösterir.

```csharp
using System;
using System.Linq;
using System.Text;
using System.Text.RegularExpressions;
using Aspose.Words;
using Aspose.Words.Fields;
using NUnit.Framework;

namespace ApiExamples
{
    public class ExReplaceHyperlinks : ApiExampleBase
    {
        public void Fields()
        {
            Document doc = new Document(MyDir + "Hyperlinks.docx");

            // Word belgelerindeki köprüler alanlardır. Köprüleri aramaya başlamak için önce tüm alanları bulmalıyız.
            // Belgedeki tüm alanları bir XPath aracılığıyla bulmak için "SelectNodes" yöntemini kullanın.
            NodeList fieldStarts = doc.SelectNodes("//FieldStart");

            foreach (FieldStart fieldStart in fieldStarts.OfType<FieldStart>())
            {
                if (fieldStart.FieldType == FieldType.FieldHyperlink)
                {
                    Hyperlink hyperlink = new Hyperlink(fieldStart);

                    // Yer imlerine bağlanan köprülerin URL'leri yoktur.
                    if (hyperlink.IsLocal)
                        continue;

                    // Her URL köprüsüne yeni bir URL ve ad verin.
                    hyperlink.Target = NewUrl;
                    hyperlink.Name = NewName;
                }
            }

            doc.Save(ArtifactsDir + "ReplaceHyperlinks.Fields.docx");
        }

        private const string NewUrl = @"http://www.aspose.com";
        private const string NewName = "Aspose - The .NET & Java Component Publisher";
    }

    /// <summary>
    /// KÖPRÜ alanları, belge gövdesinde köprüler içerir ve görüntüler. Aspose.Words'de bir alan 
    /// birkaç düğümden oluşur ve tüm bu düğümlerle doğrudan çalışmak zor olabilir. 
    /// Bu uygulama, yalnızca köprü kodu ve adının her biri yalnızca bir Çalıştırma düğümünden oluşuyorsa çalışır.
    ///
    /// Alanlar için düğüm yapısı aşağıdaki gibidir:
    /// 
    /// [FieldStart][Çalıştır - alan kodu][FieldSeparator][Çalıştır - alan sonucu][FieldEnd]
    /// 
    /// Aşağıda KÖPRÜ alanlarının iki örnek alan kodu verilmiştir:
    /// KÖPRÜ "url"
    /// KÖPRÜ \l "yer imi adı"
    /// 
    /// Bir alanın "Sonuç" özelliği, alanın belge gövdesinde kullanıcıya gösterdiği metni içerir.
    /// </summary>
    internal class Hyperlink
    {
        internal Hyperlink(FieldStart fieldStart)
        {
            if (fieldStart == null)
                throw new ArgumentNullException("fieldStart");
            if (fieldStart.FieldType != FieldType.FieldHyperlink)
                throw new ArgumentException("Field start type must be FieldHyperlink.");

            mFieldStart = fieldStart;

            // Alan ayırıcı düğümünü bulun.
            mFieldSeparator = FindNextSibling(mFieldStart, NodeType.FieldSeparator);
            if (mFieldSeparator == null)
                throw new InvalidOperationException("Cannot find field separator.");

            // Normalde, alanın son düğümünü her zaman bulabiliriz, ancak örnek belge 
            // alan sonunu koyan bir köprünün içinde bir paragraf sonu içerir 
            // sonraki paragrafta. Birkaç alana yayılan alanları işlemek çok daha karmaşık olacaktır. 
            // paragraflar doğru. Bu durumda alan sonunun boş olmasına izin vermek yeterlidir.
            mFieldEnd = FindNextSibling(mFieldSeparator, NodeType.FieldEnd);

            // Alan kodu "HYPERLINK "http:\\www.myurl.com"" gibi bir şeye benziyor, ancak birkaç çalıştırmadan oluşabilir.
            string fieldCode = GetTextSameParent(mFieldStart.NextSibling, mFieldSeparator);
            Match match = gRegex.Match(fieldCode.Trim());

            // Alan kodunda \l varsa, köprü yereldir.
            mIsLocal = match.Groups[1].Length > 0; 
            mTarget = match.Groups[2].Value;
        }

        /// <summary>
        /// Köprünün görünen adını alır veya ayarlar.
        /// </summary>
        internal string Name
        {
            get => GetTextSameParent(mFieldSeparator, mFieldEnd); 
            set
            {
                // Köprü görünen adı, bir Çalıştır olan alan sonucunda saklanır 
                // alan ayırıcı ve alan sonu arasındaki düğüm.
                Run fieldResult = (Run) mFieldSeparator.NextSibling;
                fieldResult.Text = value;

                // Alan sonucu birden fazla çalıştırmadan oluşuyorsa, bu çalıştırmaları silin.
                RemoveSameParent(fieldResult.NextSibling, mFieldEnd);
            }
        }

        /// <summary>
        /// Köprünün hedef URL'sini veya yer imi adını alır veya ayarlar.
        /// </summary>
        internal string Target
        {
            get => mTarget;
            set
            {
                mTarget = value;
                UpdateFieldCode();
            }
        }

        /// <summary>
        /// Köprü hedefi belgenin içinde bir yer imiyse doğrudur. Köprü bir URL ise yanlış.
        /// </summary>
        internal bool IsLocal
        {
            get => mIsLocal; 
            set
            {
                mIsLocal = value;
                UpdateFieldCode();
            }
        }

        private void UpdateFieldCode()
        {
            // Bir alanın alan kodu, alanın başlangıç düğümü ile alan ayırıcı arasındaki bir Çalıştırma düğümündedir.
            Run fieldCode = (Run) mFieldStart.NextSibling;
            fieldCode.Text = string.Format("HYPERLINK {0}\"{1}\"", ((mIsLocal) ? "\\l " : ""), mTarget);

            // Alan kodu birden fazla çalıştırmadan oluşuyorsa, bu çalıştırmaları silin.
            RemoveSameParent(fieldCode.NextSibling, mFieldSeparator);
        }

        /// <summary>
        /// Başlangıç düğümünden başlayarak belirtilen türde veya boş bir düğüm bulana kadar kardeşler arasında gider.
        /// </summary>
        private static Node FindNextSibling(Node startNode, NodeType nodeType)
        {
            for (Node node = startNode; node != null; node = node.NextSibling)
            {
                if (node.NodeType == nodeType)
                    return node;
            }

            return null;
        }

        /// <summary>
        /// Baştan sona metin alır, ancak son düğümü içermez.
        /// </summary>
        private static string GetTextSameParent(Node startNode, Node endNode)
        {
            if ((endNode != null) && (startNode.ParentNode != endNode.ParentNode))
                throw new ArgumentException("Start and end nodes are expected to have the same parent.");

            StringBuilder builder = new StringBuilder();
            for (Node child = startNode; !child.Equals(endNode); child = child.NextSibling)
                builder.Append(child.GetText());

            return builder.ToString();
        }

        /// <summary>
        /// Düğümleri başlangıçtan kaldırır, ancak bitiş düğümünü içermez.
        /// Başlangıç ve bitiş düğümlerinin aynı ebeveyne sahip olduğunu varsayar.
        /// </summary>
        private static void RemoveSameParent(Node startNode, Node endNode)
        {
            if (endNode != null && startNode.ParentNode != endNode.ParentNode)
                throw new ArgumentException("Start and end nodes are expected to have the same parent.");

            Node curChild = startNode;
            while ((curChild != null) && (curChild != endNode))
            {
                Node nextChild = curChild.NextSibling;
                curChild.Remove();
                curChild = nextChild;
            }
        }

        private readonly Node mFieldStart;
        private readonly Node mFieldSeparator;
        private readonly Node mFieldEnd;
        private bool mIsLocal;
        private string mTarget;

        private static readonly Regex gRegex = new Regex(
            "\\S+" + // Diğer dillerde bir veya daha fazla boşluk olmayan HYPERLINK veya başka bir kelime.
            "\\s+" + // Bir veya daha fazla boşluk.
            "(?:\"\"\\s+)?" + // Yakalamayan isteğe bağlı "" ve bir veya daha fazla boşluk.
            "(\\\\l\\s+)?" + // İsteğe bağlı \l bayrağının ardından bir veya daha fazla boşluk.
            "\"" + // Bir kesme işareti.    
            "([^\"]+)" + // Kesme işareti (köprü hedefi) hariç bir veya daha fazla karakter.
            "\"" // Bir kapanış kesme işareti.
        );
    }
}
```

### Ayrıca bakınız

* class [Node](../node/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
