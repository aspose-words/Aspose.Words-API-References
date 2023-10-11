---
title: Class NodeList
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.NodeList sınıf. kullanılarak yürütülen bir XPath sorgusuyla eşleşen düğümlerin bir koleksiyonunu temsil eder.SelectNodes yöntem.
type: docs
weight: 4220
url: /tr/net/aspose.words/nodelist/
---
## NodeList class

kullanılarak yürütülen bir XPath sorgusuyla eşleşen düğümlerin bir koleksiyonunu temsil eder.[`SelectNodes`](../compositenode/selectnodes/) yöntem.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Aspose.Words Belge Nesne Modeli (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) dokümantasyon makalesi.

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
| [GetEnumerator](../../aspose.words/nodelist/getenumerator/)() | Düğümlerin koleksiyonu üzerinde basit bir "foreach" stili yinelemesi sağlar. |
| [ToArray](../../aspose.words/nodelist/toarray/)() | Koleksiyondaki tüm düğümleri yeni bir düğüm dizisine kopyalar. |

### Notlar

`NodeList` tarafından iade edilir[`SelectNodes`](../compositenode/selectnodes/) ve XPath sorgusuyla eşleşen bir koleksiyon düğüm içerir.

`NodeList` indekslenmiş erişimi ve yinelemeyi destekler.

Tedavi et`NodeList` koleksiyonu bir "anlık görüntü" koleksiyonu olarak.`NodeList`başlar , "canlı" bir koleksiyon olarak başlar çünkü XPath sorgusu çalıştırıldığında düğümler gerçekte alınmaz. Düğümler yalnızca erişim üzerine alınır ve şu anda düğüm ve ondan önceki tüm düğümler, bir "anlık görüntü" koleksiyonu oluşturacak şekilde önbelleğe alınır.

### Örnekler

Bir Word belgesindeki tüm köprülerin nasıl bulunacağını ve ardından URL'lerinin ve görünen adlarının nasıl değiştirileceğini gösterir.

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

                    // Yer imlerine bağlantı veren köprülerin URL'leri yoktur.
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

     ///<summary>
      ///KÖPRÜ alanları belge gövdesindeki köprüleri içerir ve görüntüler. Aspose.Words'te bir alan
      ///birden fazla düğümden oluşur ve tüm bu düğümlerle doğrudan çalışmak zor olabilir.
     ///Bu uygulama yalnızca köprü kodu ve adının her biri yalnızca bir Çalıştırma düğümünden oluşuyorsa çalışır.
    ///
     ///Alanların düğüm yapısı aşağıdaki gibidir:
     ///
     ///[FieldStart][Run - field code][FieldSeparator][Run - field result][FieldEnd]
     ///
     ///Below are two example field codes of HYPERLINK fields:
     ///HYPERLINK "url"
     ///HYPERLINK \l "bookmark name"
     ///
     ///A field's "Result" property contains text that the field displays in the document body to the user.
     ///</summary>
    internal class Hyperlink
    {
        internal Hyperlink(FieldStart fieldStart)
        {
            if (fieldStart == null)
                throw new ArgumentNullException("fieldStart");
            if (fieldStart.FieldType != FieldType.FieldHyperlink)
                throw new ArgumentException("Field start type must be FieldHyperlink.");

            mFieldStart = fieldStart;

            // Alan ayırıcı düğümü bulun.
            mFieldSeparator = FindNextSibling(mFieldStart, NodeType.FieldSeparator);
            if (mFieldSeparator == null)
                throw new InvalidOperationException("Cannot find field separator.");

             // Normalde alanın bitiş düğümünü her zaman bulabiliriz ancak örnek belge
             // bir köprünün içinde, alanı sona erdiren bir paragraf sonu içerir
            // sonraki paragrafta. Birkaç alanı kapsayan alanları yönetmek çok daha karmaşık olacaktır.
            //paragrafları doğru şekilde yaz. Bu durumda alan sonunun null olmasına izin vermek yeterlidir.
            mFieldEnd = FindNextSibling(mFieldSeparator, NodeType.FieldEnd);

            // Alan kodu "HYPERLINK "http:\\www.myurl.com"" gibi görünür, ancak birkaç çalıştırmadan oluşabilir.
            string fieldCode = GetTextSameParent(mFieldStart.NextSibling, mFieldSeparator);
            Match match = gRegex.Match(fieldCode.Trim());

            // Alan kodunda \l mevcutsa köprü yereldir.
            mIsLocal = match.Groups[1].Length > 0; 
            mTarget = match.Groups[2].Value;
        }

         ///<summary>
         ///Gets or sets the display name of the hyperlink.
         ///</summary>
        internal string Name
        {
            get => GetTextSameParent(mFieldSeparator, mFieldEnd); 
            set
            {
                 // Köprü görünen adı, Çalıştırma olan alan sonucunda saklanır
                // alan ayırıcı ile alan sonu arasındaki düğüm.
                Run fieldResult = (Run) mFieldSeparator.NextSibling;
                fieldResult.Text = value;

                // Saha sonucu birden fazla çalıştırmadan oluşuyorsa bu çalıştırmaları silin.
                RemoveSameParent(fieldResult.NextSibling, mFieldEnd);
            }
        }

         ///<summary>
         ///Gets or sets the target URL or bookmark name of the hyperlink.
         ///</summary>
        internal string Target
        {
            get => mTarget;
            set
            {
                mTarget = value;
                UpdateFieldCode();
            }
        }

         ///<summary>
         ///True if the hyperlinks target is a bookmark inside the document. False if the hyperlink is a URL.
         ///</summary>
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

            // Alan kodu birden fazla çalıştırmadan oluşuyorsa bu çalıştırmaları silin.
            RemoveSameParent(fieldCode.NextSibling, mFieldSeparator);
        }

         ///<summary>
         ///Goes through siblings starting from the start node until it finds a node of the specified type or null.
         ///</summary>
        private static Node FindNextSibling(Node startNode, NodeType nodeType)
        {
            for (Node node = startNode; node != null; node = node.NextSibling)
            {
                if (node.NodeType == nodeType)
                    return node;
            }

            return null;
        }

         ///<summary>
         ///Retrieves text from start up to but not including the end node.
         ///</summary>
        private static string GetTextSameParent(Node startNode, Node endNode)
        {
            if ((endNode != null) && (startNode.ParentNode != endNode.ParentNode))
                throw new ArgumentException("Start and end nodes are expected to have the same parent.");

            StringBuilder builder = new StringBuilder();
            for (Node child = startNode; !child.Equals(endNode); child = child.NextSibling)
                builder.Append(child.GetText());

            return builder.ToString();
        }

         ///<summary>
         ///Removes nodes from start up to but not including the end node.
         ///Assumes that the start and end nodes have the same parent.
         ///</summary>
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
            "\\S+" + // Bir veya daha fazla boşluksuz HYPERLINK veya diğer dillerdeki başka bir kelime.
            "\\s+" + // Bir veya daha fazla boşluk.
            "(?:\"\"\\s+)?" + // İsteğe bağlı "" ve bir veya daha fazla boşluğu yakalamayan.
            "(\\\\l\\s+)?" + // İsteğe bağlı \l bayrağı ve ardından bir veya daha fazla boşluk.
            "\"" +  // Bir kesme işareti.
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


