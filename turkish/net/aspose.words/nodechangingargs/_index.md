---
title: NodeChangingArgs Class
linktitle: NodeChangingArgs
articleTitle: NodeChangingArgs
second_title: Aspose.Words for .NET
description: Aspose.Words.NodeChangingArgs sınıf. Yöntemler için veri sağlarINodeChangingCallback arayüz C#'da.
type: docs
weight: 4190
url: /tr/net/aspose.words/nodechangingargs/
---
## NodeChangingArgs class

Yöntemler için veri sağlar[`INodeChangingCallback`](../inodechangingcallback/) arayüz.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Aspose.Words Belge Nesne Modeli (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) dokümantasyon makalesi.

```csharp
public class NodeChangingArgs
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Action](../../aspose.words/nodechangingargs/action/) { get; } | Ne tür bir düğüm değişikliği olayının meydana geldiğini gösteren bir değer alır. |
| [NewParent](../../aspose.words/nodechangingargs/newparent/) { get; } | İşlem tamamlandıktan sonra ayarlanacak düğümün ebeveynini alır. |
| [Node](../../aspose.words/nodechangingargs/node/) { get; } | Alır[`Node`](./node/) bu ekleniyor veya kaldırılıyor. |
| [OldParent](../../aspose.words/nodechangingargs/oldparent/) { get; } | İşlem başlamadan önce düğümün ebeveynini alır. |

## Örnekler

Bir geri aramayla düğüm değişiminin nasıl özelleştirileceğini gösterir.

```csharp
public void FontChangeViaCallback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Düğüm değiştirme geri çağrısını özel uygulamaya ayarlayın,
    // ardından bir günlük oluşturmasını sağlamak için düğümleri ekleyin/kaldırın.
    HandleNodeChangingFontChanger callback = new HandleNodeChangingFontChanger();
    doc.NodeChangingCallback = callback;

    builder.Writeln("Hello world!");
    builder.Writeln("Hello again!");
    builder.InsertField(" HYPERLINK \"https://www.google.com/\" ");
    builder.InsertShape(ShapeType.Rectangle, 300, 300);

    doc.Range.Fields[0].Remove();

    Console.WriteLine(callback.GetLog());
}

/// <summary>
/// Her düğüm ekleme ve çıkarma işleminin tarihini ve saatini günlüğe kaydeder.
/// Çalıştırma düğümlerinin metin içerikleri için özel bir yazı tipi adı/boyutu ayarlar.
/// </summary>
public class HandleNodeChangingFontChanger : INodeChangingCallback
{
    void INodeChangingCallback.NodeInserted(NodeChangingArgs args)
    {
        mLog.AppendLine($"\tType:\t{args.Node.NodeType}");
        mLog.AppendLine($"\tHash:\t{args.Node.GetHashCode()}");

        if (args.Node.NodeType == NodeType.Run)
        {
            Aspose.Words.Font font = ((Run) args.Node).Font;
            mLog.Append($"\tFont:\tChanged from \"{font.Name}\" {font.Size}pt");

            font.Size = 24;
            font.Name = "Arial";

            mLog.AppendLine($" to \"{font.Name}\" {font.Size}pt");
            mLog.AppendLine($"\tContents:\n\t\t\"{args.Node.GetText()}\"");
        }
    }

    void INodeChangingCallback.NodeInserting(NodeChangingArgs args)
    {
        mLog.AppendLine($"\n{DateTime.Now:dd/MM/yyyy HH:mm:ss:fff}\tNode insertion:");
    }

    void INodeChangingCallback.NodeRemoved(NodeChangingArgs args)
    {
        mLog.AppendLine($"\tType:\t{args.Node.NodeType}");
        mLog.AppendLine($"\tHash code:\t{args.Node.GetHashCode()}");
    }

    void INodeChangingCallback.NodeRemoving(NodeChangingArgs args)
    {
        mLog.AppendLine($"\n{DateTime.Now:dd/MM/yyyy HH:mm:ss:fff}\tNode removal:");
    }

    public string GetLog()
    {
        return mLog.ToString();
    }

    private readonly StringBuilder mLog = new StringBuilder();
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
