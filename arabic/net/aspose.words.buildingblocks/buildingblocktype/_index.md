---
title: BuildingBlockType Enum
linktitle: BuildingBlockType
articleTitle: BuildingBlockType
second_title: Aspose.Words لـ .NET
description: Aspose.Words.BuildingBlocks.BuildingBlockType تعداد. يحدد نوع الكتلة البرمجية الإنشائية. قد يؤثر النوع على رؤية وسلوك الكتلة البرمجية الإنشائية في Microsoft Word في C#.
type: docs
weight: 170
url: /ar/net/aspose.words.buildingblocks/buildingblocktype/
---
## BuildingBlockType enumeration

يحدد نوع الكتلة البرمجية الإنشائية. قد يؤثر النوع على رؤية وسلوك الكتلة البرمجية الإنشائية في Microsoft Word.

```csharp
public enum BuildingBlockType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | لم يتم تحديد معلومات النوع للكتلة البرمجية الإنشائية. |
| AutomaticallyReplaceNameWithContent | `1` | يسمح بإدراج الكتلة البرمجية الإنشائية تلقائيًا في المستند عند يتم إدخال اسمها في التطبيق. |
| StructuredDocumentTagPlaceholderText | `2` | الكتلة البرمجية الإنشائية عبارة عن نص العنصر النائب لعلامة مستند منظمة. |
| FormFieldHelpText | `3` | الكتلة البرمجية الإنشائية عبارة عن نص تعليمات لحقل النموذج. |
| Normal | `4` | العنصر الأساسي عبارة عن إدخال مستند عادي (أي عادي). |
| AutoCorrect | `5` | الكتلة البرمجية الإنشائية مرتبطة بأدوات التدقيق الإملائي والنحوي. |
| AutoText | `6` | الكتلة البرمجية الإنشائية عبارة عن إدخال نص تلقائي. |
| All | `7` | الكتلة البرمجية الإنشائية مرتبطة بجميع الأنواع. |
| Default | `0` | حفظ باسمNone . |

## ملاحظات

يتوافق مع**ST_DocPartType** اكتب OOXML.

## أمثلة

يوضح كيفية إضافة كتلة إنشاء مخصصة إلى مستند.

```csharp
public void CreateAndInsert()
{
    // يقوم مستند قاموس المصطلحات الخاص بالمستند بتخزين الكتل البرمجية الإنشائية.
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();
    doc.GlossaryDocument = glossaryDoc;

    // قم بإنشاء كتلة إنشاء، وقم بتسميتها، ثم قم بإضافتها إلى مستند المسرد.
    BuildingBlock block = new BuildingBlock(glossaryDoc)
    {
        Name = "Custom Block"
    };

    glossaryDoc.AppendChild(block);

    // جميع المعرفات الفريدة العمومية (GUIDs) الجديدة لها نفس القيمة الصفرية افتراضيًا، ويمكننا منحها قيمة فريدة جديدة.
    Assert.AreEqual("00000000-0000-0000-0000-000000000000", block.Guid.ToString());

    block.Guid = Guid.NewGuid();

    // الخصائص التالية تصنف الكتل البرمجية الإنشائية
    // في القائمة التي يمكننا الوصول إليها في Microsoft Word عبر "إدراج" -> "الأجزاء السريعة" -> “منظم لبنات البناء”.
    Assert.AreEqual("(Empty Category)", block.Category);
    Assert.AreEqual(BuildingBlockType.None, block.Type);
    Assert.AreEqual(BuildingBlockGallery.All, block.Gallery);
    Assert.AreEqual(BuildingBlockBehavior.Content, block.Behavior);

    // قبل أن نتمكن من إضافة هذه الكتلة البرمجية الإنشائية إلى مستندنا، سنحتاج إلى إعطائها بعض المحتويات،
    // وهو ما سنفعله باستخدام زائر المستند. سيقوم هذا الزائر أيضًا بتعيين فئة ومعرض وسلوك.
    BuildingBlockVisitor visitor = new BuildingBlockVisitor(glossaryDoc);
    block.Accept(visitor);

    // يمكننا الوصول إلى الكتلة التي أنشأناها للتو من مستند المسرد.
    BuildingBlock customBlock = glossaryDoc.GetBuildingBlock(BuildingBlockGallery.QuickParts,
        "My custom building blocks", "Custom Block");

    // الكتلة نفسها عبارة عن قسم يحتوي على النص.
    Assert.AreEqual($"Text inside {customBlock.Name}\f", customBlock.FirstSection.Body.FirstParagraph.GetText());
    Assert.AreEqual(customBlock.FirstSection, customBlock.LastSection);
    // الآن يمكننا إدراجه في المستند كقسم جديد.
    doc.AppendChild(doc.ImportNode(customBlock.FirstSection, true));

    // يمكننا أيضًا العثور عليه في Building Blocks Organizer الخاص بـ Microsoft Word ووضعه يدويًا.
    doc.Save(ArtifactsDir + "BuildingBlocks.CreateAndInsert.dotx");
}

/// <summary>
/// إعداد الكتلة البرمجية الإنشائية التي تمت زيارتها لإدراجها في المستند كجزء سريع وإضافة نص إلى محتوياتها.
/// </summary>
public class BuildingBlockVisitor : DocumentVisitor
{
    public BuildingBlockVisitor(GlossaryDocument ownerGlossaryDoc)
    {
        mBuilder = new StringBuilder();
        mGlossaryDoc = ownerGlossaryDoc;
    }

    public override VisitorAction VisitBuildingBlockStart(BuildingBlock block)
    {
        // قم بتكوين الكتلة البرمجية الإنشائية كجزء سريع، وأضف الخصائص المستخدمة بواسطة Building Blocks Organizer.
        block.Behavior = BuildingBlockBehavior.Paragraph;
        block.Category = "My custom building blocks";
        block.Description =
            "Using this block in the Quick Parts section of word will place its contents at the cursor.";
        block.Gallery = BuildingBlockGallery.QuickParts;

        // أضف قسمًا يحتوي على نص.
        // سيؤدي إدراج الكتلة في المستند إلى إلحاق هذا القسم بعقده الفرعية في الموقع.
        Section section = new Section(mGlossaryDoc);
        block.AppendChild(section);
        block.FirstSection.EnsureMinimum();

        Run run = new Run(mGlossaryDoc, "Text inside " + block.Name);
        block.FirstSection.Body.FirstParagraph.AppendChild(run);

        return VisitorAction.Continue;
    }

    public override VisitorAction VisitBuildingBlockEnd(BuildingBlock block)
    {
        mBuilder.Append("Visited " + block.Name + "\r\n");
        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
    private readonly GlossaryDocument mGlossaryDoc;
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks/)
* المجسم [Aspose.Words](../../)
