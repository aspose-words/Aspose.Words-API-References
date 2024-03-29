---
title: NodeChangingArgs Class
linktitle: NodeChangingArgs
articleTitle: NodeChangingArgs
second_title: Aspose.Words لـ .NET
description: Aspose.Words.NodeChangingArgs فصل. يوفر بيانات عن طرقINodeChangingCallback الواجهة في C#.
type: docs
weight: 4190
url: /ar/net/aspose.words/nodechangingargs/
---
## NodeChangingArgs class

يوفر بيانات عن طرق[`INodeChangingCallback`](../inodechangingcallback/) الواجهة.

لمعرفة المزيد، قم بزيارة[نموذج كائن مستند Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) مقالة توثيقية.

```csharp
public class NodeChangingArgs
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Action](../../aspose.words/nodechangingargs/action/) { get; } | الحصول على قيمة تشير إلى نوع حدث تغيير العقدة الذي يحدث. |
| [NewParent](../../aspose.words/nodechangingargs/newparent/) { get; } | يحصل على أصل العقدة الذي سيتم تعيينه بعد اكتمال العملية. |
| [Node](../../aspose.words/nodechangingargs/node/) { get; } | يحصل على[`Node`](./node/) التي تتم إضافتها أو إزالتها. |
| [OldParent](../../aspose.words/nodechangingargs/oldparent/) { get; } | الحصول على أصل العقدة قبل بدء العملية. |

## أمثلة

يوضح كيفية تخصيص تغيير العقدة من خلال رد الاتصال.

```csharp
public void FontChangeViaCallback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // قم بتعيين رد الاتصال المتغير للعقدة على التنفيذ المخصص،
    // ثم قم بإضافة/إزالة العقد للحصول على سجل.
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
/// يسجل تاريخ ووقت كل إدخال وإزالة للعقدة.
/// يعين اسم/حجم خط مخصص لمحتويات النص في عقد التشغيل.
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

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
