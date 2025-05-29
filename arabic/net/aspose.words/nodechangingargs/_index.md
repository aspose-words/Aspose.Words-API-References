---
title: NodeChangingArgs Class
linktitle: NodeChangingArgs
articleTitle: NodeChangingArgs
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.NodeChangingArgs، المصممة لتحسين معالجة مستنداتك من خلال تكامل سلس مع INodeChangingCallback. حسّن سير عملك اليوم!
type: docs
weight: 4880
url: /ar/net/aspose.words/nodechangingargs/
---
## NodeChangingArgs class

يوفر بيانات لأساليب[`INodeChangingCallback`](../inodechangingcallback/) الواجهة.

لمعرفة المزيد، قم بزيارة[نموذج كائن المستند (DOM) في Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) مقالة توثيقية.

```csharp
public class NodeChangingArgs
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Action](../../aspose.words/nodechangingargs/action/) { get; } | يحصل على قيمة تشير إلى نوع حدث تغيير العقدة الذي يحدث. |
| [NewParent](../../aspose.words/nodechangingargs/newparent/) { get; } | يحصل على العقدة الأصلية التي سيتم تعيينها بعد اكتمال العملية. |
| [Node](../../aspose.words/nodechangingargs/node/) { get; } | يحصل على[`Node`](./node/) الذي يتم إضافته أو إزالته. |
| [OldParent](../../aspose.words/nodechangingargs/oldparent/) { get; } | يحصل على العقدة الأصلية قبل بدء العملية. |

## أمثلة

يوضح كيفية تخصيص تغيير العقدة باستخدام معاودة الاتصال.

```csharp
public void FontChangeViaCallback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // تعيين معاودة الاتصال لتغيير العقدة إلى التنفيذ المخصص،
    // ثم قم بإضافة/إزالة العقد حتى تتمكن من إنشاء سجل.
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
/// يسجل التاريخ والوقت لكل إدخال وإزالة للعقدة.
/// تعيين اسم/حجم خط مخصص لمحتويات النص الخاصة بعقد التشغيل.
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

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
