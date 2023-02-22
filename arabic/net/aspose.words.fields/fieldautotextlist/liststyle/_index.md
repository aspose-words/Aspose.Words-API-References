---
title: FieldAutoTextList.ListStyle
second_title: Aspose.Words لمراجع .NET API
description: FieldAutoTextList ملكية. الحصول على أو تحديد اسم النمط الذي تستند إليه القائمة التي ستحتوي على الإدخالات .
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldautotextlist/liststyle/
---
## FieldAutoTextList.ListStyle property

الحصول على أو تحديد اسم النمط الذي تستند إليه القائمة التي ستحتوي على الإدخالات .

```csharp
public string ListStyle { get; set; }
```

### أمثلة

يوضح كيفية استخدام حقل AUTOTEXTLIST للاختيار من قائمة إدخالات النص التلقائي.

```csharp
{
    Document doc = new Document();

    // إنشاء مستند مسرد وتعبئته بإدخالات نصية آلية.
    doc.GlossaryDocument = new GlossaryDocument();
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 1", "Contents of AutoText 1");
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 2", "Contents of AutoText 2");
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 3", "Contents of AutoText 3");

    DocumentBuilder builder = new DocumentBuilder(doc);

    // قم بإنشاء حقل AUTOTEXTLIST وعيّن النص الذي سيعرضه الحقل في Microsoft Word.
    // قم بتعيين النص لمطالبة المستخدم بالنقر بزر الماوس الأيمن فوق هذا الحقل لتحديد كتلة إنشاء نص تلقائي ،
    // الذي سيتم عرض محتوياته في الحقل.
    FieldAutoTextList field = (FieldAutoTextList)builder.InsertField(FieldType.FieldAutoTextList, true);
    field.EntryName = "Right click here to select an AutoText block";
    field.ListStyle = "Heading 1";
    field.ScreenTip = "Hover tip text for AutoTextList goes here";

    Assert.AreEqual(" AUTOTEXTLIST  \"Right click here to select an AutoText block\" " +
                    "\\s \"Heading 1\" " +
                    "\\t \"Hover tip text for AutoTextList goes here\"", field.GetFieldCode());

    doc.Save(ArtifactsDir + "Field.AUTOTEXTLIST.dotx");

/// <summary>
/// إنشاء كتلة إنشاء من نوع النص التلقائي وإضافتها إلى مستند مسرد.
/// </summary>
private static void AppendAutoTextEntry(GlossaryDocument glossaryDoc, string name, string contents)
{
    BuildingBlock buildingBlock = new BuildingBlock(glossaryDoc);
    buildingBlock.Name = name;
    buildingBlock.Gallery = BuildingBlockGallery.AutoText;
    buildingBlock.Category = "General";
    buildingBlock.Behavior = BuildingBlockBehavior.Paragraph;

    Section section = new Section(glossaryDoc);
    section.AppendChild(new Body(glossaryDoc));
    section.Body.AppendParagraph(contents);
    buildingBlock.AppendChild(section);

    glossaryDoc.AppendChild(buildingBlock);
}
```

### أنظر أيضا

* class [FieldAutoTextList](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldautotextlist/)
* المجسم [Aspose.Words](../../../)


