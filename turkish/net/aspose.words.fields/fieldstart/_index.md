---
title: FieldStart Class
linktitle: FieldStart
articleTitle: FieldStart
second_title: Aspose.Words for .NET
description: Aspose.Words.Fields.FieldStart sınıf. Belgedeki Word alanının başlangıcını temsil eder C#'da.
type: docs
weight: 2430
url: /tr/net/aspose.words.fields/fieldstart/
---
## FieldStart class

Belgedeki Word alanının başlangıcını temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Alanlarla Çalışmak](https://docs.aspose.com/words/net/working-with-fields/) dokümantasyon makalesi.

```csharp
public class FieldStart : FieldChar
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [FieldData](../../aspose.words.fields/fieldstart/fielddata/) { get; } | Alanla ilişkili özel alan verilerini alır. |
| [FieldType](../../aspose.words.fields/fieldchar/fieldtype/) { get; } | Alanın türünü döndürür. |
| [Font](../../aspose.words/inline/font/) { get; } | Bu nesnenin yazı tipi formatlamasına erişim sağlar. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | İadeler`doğru` bu düğüm başka düğümler içeriyorsa. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Değişiklik izleme etkinken bu nesne Microsoft Word'de silinmişse true değerini döndürür. |
| [IsDirty](../../aspose.words.fields/fieldchar/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Microsoft Word'de değişiklik izleme etkinken nesnenin biçimlendirmesi değiştirilmişse doğru değerini döndürür. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Bu nesne Microsoft Word'e değişiklik izleme etkinken eklenmişse doğru değerini döndürür. |
| [IsLocked](../../aspose.words.fields/fieldchar/islocked/) { get; set; } | Ana alanın kilitli olup olmadığını alır veya ayarlar (sonucu yeniden hesaplanmamalıdır). |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | İadeler`doğru` değişiklik izleme etkinken bu nesne Microsoft Word'de taşındıysa (silindiyse). |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | İadeler`doğru` bu nesne Microsoft Word'de değişiklik izleme etkinken taşınmışsa (eklenmişse). |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümden hemen sonra gelen düğümü alır. |
| override [NodeType](../../aspose.words.fields/fieldstart/nodetype/) { get; } | İadelerFieldStart . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün doğrudan ebeveynini alır. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Üst öğeyi alır[`Paragraph`](../../aspose.words/paragraph/) bu düğümün. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir değeri döndürür[`Range`](../../aspose.words/range/) Bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words.fields/fieldstart/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Ziyaretçi kabul eder. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Düğümün bir kopyasını oluşturur. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Belirtilenin ilk atayı alır[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Belirtilen nesne türünün ilk atayı alır. |
| [GetField](../../aspose.words.fields/fieldchar/getfield/)() | char. alanı için bir alan döndürür |
| override [GetText](../../aspose.words/specialchar/gettext/)() | Bu düğümün temsil ettiği özel karakteri alır. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Ön sipariş ağaç geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendini üst öğeden kaldırır. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Düğümün içeriğini belirtilen formatta bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

## Notlar

`FieldStart` satır içi düzeyde bir düğümdür ve the ile temsil edilir[`FieldStartChar`](../../aspose.words/controlchar/fieldstartchar/) Belgedeki kontrol karakteri.

`FieldStart` sadece çocuğu olabilir[`Paragraph`](../../aspose.words/paragraph/).

Microsoft Word belgesindeki tam alan, bir alan başlangıç karakteri, alan kodu, alan ayırıcı karakteri, alan result ve alan sonu karakterinden oluşan karmaşık bir yapıdır. Bazı alanlarda yalnızca alan başlangıcı, alan kodu ve alan sonu bulunur.

Belgeye kolayca yeni bir alan eklemek için[`InsertField`](../../aspose.words/documentbuilder/insertfield/) yöntemi.

## Örnekler

Bir alan koleksiyonuyla nasıl çalışılacağını gösterir.

```csharp
public void FieldCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
    builder.InsertField(" TIME ");
    builder.InsertField(" REVNUM ");
    builder.InsertField(" AUTHOR  \"John Doe\" ");
    builder.InsertField(" SUBJECT \"My Subject\" ");
    builder.InsertField(" QUOTE \"Hello world!\" ");
    doc.UpdateFields();

    FieldCollection fields = doc.Range.Fields;

    Assert.AreEqual(6, fields.Count);

    // Alan koleksiyonu üzerinde yineleme yapın ve içerikleri yazdırıp yazın
    // özel bir ziyaretçi uygulaması kullanarak her alanın.
    FieldVisitor fieldVisitor = new FieldVisitor();

    using (IEnumerator<Field> fieldEnumerator = fields.GetEnumerator())
    {
        while (fieldEnumerator.MoveNext())
        {
            if (fieldEnumerator.Current != null)
            {
                fieldEnumerator.Current.Start.Accept(fieldVisitor);
                fieldEnumerator.Current.Separator?.Accept(fieldVisitor);
                fieldEnumerator.Current.End.Accept(fieldVisitor);
            }
            else
            {
                Console.WriteLine("There are no fields in the document.");
            }
        }
    }

    Console.WriteLine(fieldVisitor.GetText());
}

/// <summary>
/// Alan bilgilerini yazdıran ziyaretçi uygulamasını belgeleyin.
/// </summary>
public class FieldVisitor : DocumentVisitor
{
    public FieldVisitor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Ziyaretçinin biriktirdiği belgenin düz metnini alır.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Belgede bir FieldStart düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        mBuilder.AppendLine("Found field: " + fieldStart.FieldType);
        mBuilder.AppendLine("\tField code: " + fieldStart.GetField().GetFieldCode());
        mBuilder.AppendLine("\tDisplayed as: " + fieldStart.GetField().Result);

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede FieldSeparator düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        mBuilder.AppendLine("\tFound separator: " + fieldSeparator.GetText());

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede FieldEnd düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        mBuilder.AppendLine("End of field: " + fieldEnd.FieldType);

        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
}
```

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

* class [FieldChar](../fieldchar/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
