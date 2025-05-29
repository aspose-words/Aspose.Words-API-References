---
title: DocumentBase.NodeChangingCallback
linktitle: NodeChangingCallback
articleTitle: NodeChangingCallback
second_title: .NET için Aspose.Words
description: Düğüm ekleme veya kaldırma işlemlerinde tetiklenen, belge yönetimini ve iş akışı verimliliğini artıran DocumentBase NodeChangingCallback özelliğini keşfedin.
type: docs
weight: 60
url: /tr/net/aspose.words/documentbase/nodechangingcallback/
---
## DocumentBase.NodeChangingCallback property

Belgeye bir düğüm eklendiğinde veya kaldırıldığında çağrılır.

```csharp
public INodeChangingCallback NodeChangingCallback { get; set; }
```

## Örnekler

Geri arama ile düğüm değişiminin nasıl özelleştirileceğini gösterir.

```csharp
public void FontChangeViaCallback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Düğüm değiştirme geri aramasını özel uygulamaya ayarlayın,
    // daha sonra bir günlük oluşturması için düğümleri ekleyin/kaldırın.
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
/// Her düğümün eklenmesi ve kaldırılmasının tarih ve saatini günlüğe kaydeder.
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
            Aspose.Words.Font font = ((Run)args.Node).Font;
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

* interface [INodeChangingCallback](../../inodechangingcallback/)
* class [DocumentBase](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
