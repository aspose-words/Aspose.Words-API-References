---
title: INodeChangingCallback Interface
linktitle: INodeChangingCallback
articleTitle: INodeChangingCallback
second_title: Aspose.Words for .NET
description: Aspose.Words.INodeChangingCallback arayüz. Belgeye düğümler eklendiğinde veya kaldırıldığında bildirim almak istiyorsanız bu arayüzü uygulayın C#'da.
type: docs
weight: 3200
url: /tr/net/aspose.words/inodechangingcallback/
---
## INodeChangingCallback interface

Belgeye düğümler eklendiğinde veya kaldırıldığında bildirim almak istiyorsanız bu arayüzü uygulayın.

```csharp
public interface INodeChangingCallback
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| [NodeInserted](../../aspose.words/inodechangingcallback/nodeinserted/)(*[NodeChangingArgs](../nodechangingargs/)*) | Bu belgeye ait bir düğüm başka bir düğüme eklendiğinde çağrılır. |
| [NodeInserting](../../aspose.words/inodechangingcallback/nodeinserting/)(*[NodeChangingArgs](../nodechangingargs/)*) | Bu belgeye ait bir düğümün başka bir düğüme eklenmesinden hemen önce çağrılır. |
| [NodeRemoved](../../aspose.words/inodechangingcallback/noderemoved/)(*[NodeChangingArgs](../nodechangingargs/)*) | Bu belgeye ait bir düğüm üst öğesinden kaldırıldığında çağrılır. |
| [NodeRemoving](../../aspose.words/inodechangingcallback/noderemoving/)(*[NodeChangingArgs](../nodechangingargs/)*) | Bu belgeye ait bir düğümün belgeden kaldırılmasından hemen önce çağrılır. |

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
