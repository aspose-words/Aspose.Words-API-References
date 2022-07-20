---
title: GlossaryDocument
second_title: Aspose.Words لمراجع .NET API
description: يمثل العنصر الجذر لمستند قاموس المصطلحات داخل مستند Word. _ x000d_ مستند المسرد هو تخزين للنص التلقائي وإدخالات التصحيح التلقائي وكتل الإنشاء.
type: docs
weight: 170
url: /ar/net/aspose.words.buildingblocks/glossarydocument/
---
## GlossaryDocument class

يمثل العنصر الجذر لمستند قاموس المصطلحات داخل مستند Word. _ x000d_ مستند المسرد هو تخزين للنص التلقائي وإدخالات التصحيح التلقائي وكتل الإنشاء.

```csharp
public class GlossaryDocument : DocumentBase
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [GlossaryDocument](glossarydocument)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape) { get; set; } | الحصول على أو تحديد شكل خلفية المستند. يمكن أن يكون فارغًا. |
| [BuildingBlocks](../../aspose.words.buildingblocks/glossarydocument/buildingblocks) { get; } | إرجاع مجموعة مكتوبة تمثل كل الكتل الإنشائية في مستند قاموس المصطلحات. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | يحصل على جميع العقد الفرعية الفورية لهذه العقدة. |
| [Count](../../aspose.words/compositenode/count) { get; } | الحصول على عدد الأطفال المباشرين لهذه العقدة. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | يحدد معرف العقدة المخصص ._ x000d_ |
| override [Document](../../aspose.words/documentbase/document) { get; } |  |
| [FirstBuildingBlock](../../aspose.words.buildingblocks/glossarydocument/firstbuildingblock) { get; } | الحصول على اللبنة البرمجية الإنشائية الأولى في مستند المسرد. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | الحصول على الطفل الأول للعقدة . |
| [FontInfos](../../aspose.words/documentbase/fontinfos) { get; } | يوفر الوصول إلى خصائص الخطوط المستخدمة في هذا المستند. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | إرجاع صحيح إذا كانت هذه العقدة بها أي عقد فرعية. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | إرجاع صحيح لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [LastBuildingBlock](../../aspose.words.buildingblocks/glossarydocument/lastbuildingblock) { get; } | الحصول على الكتلة البرمجية الإنشائية الأخيرة في مستند المسرد. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | الحصول على آخر تابع للعقدة . |
| [Lists](../../aspose.words/documentbase/lists) { get; } | يوفر الوصول إلى تنسيق القائمة المستخدم في المستند. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback) { get; set; } | يتم استدعائها عند إدراج عقدة أو إزالتها في المستند. |
| override [NodeType](../../aspose.words.buildingblocks/glossarydocument/nodetype) { get; } | إرجاع ملفGlossaryDocument القيمة ._ x000d_ |
| [PageColor](../../aspose.words/documentbase/pagecolor) { get; set; } | الحصول على أو تحديد لون صفحة المستند. هذه الخاصية هي نسخة أبسط من[`BackgroundShape`](../../aspose.words/documentbase/backgroundshape) . |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | الحصول على الأصل المباشر لهذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [Range](../../aspose.words/node/range) { get; } | إرجاع أ **نطاق** الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback) { get; set; } | يسمح بالتحكم في كيفية تحميل الموارد الخارجية. |
| [Styles](../../aspose.words/documentbase/styles) { get; } | إرجاع مجموعة من الأنماط المحددة في المستند. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback) { get; set; } | يتم استدعاؤه أثناء إجراءات معالجة المستندات المختلفة عند اكتشاف مشكلة قد تؤدي إلى في البيانات أو فقدان الدقة في التنسيق ._ x000d_ |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words.buildingblocks/glossarydocument/accept)(DocumentVisitor) | يقبل الزائر . |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | يضيف العقدة المحددة إلى نهاية قائمة العقد الفرعية لهذه العقدة . |
| [Clone](../../aspose.words/node/clone)(bool) | لإنشاء نسخة مكررة من العقدة . |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | محجوز لاستخدام النظام. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | يحصل على أول سلف محدد[`NodeType`](../../aspose.words/nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | الحصول على الأصل الأول لنوع الكائن المحدد. |
| [GetBuildingBlock](../../aspose.words.buildingblocks/glossarydocument/getbuildingblock)(BuildingBlockGallery, string, string) | البحث عن كتلة إنشاء باستخدام المعرض والفئة والاسم المحدد. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | إرجاع العقدة الفرعية رقم N التي تطابق النوع المحدد. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | إرجاع مجموعة مباشرة من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | يوفر دعمًا لكل تكرار نمط على العقد التابعة لهذه العقدة ._ x000d_ |
| override [GetText](../../aspose.words/compositenode/gettext)() | يحصل على نص هذه العقدة وجميع توابعها. |
| [ImportNode](../../aspose.words/documentbase/importnode)(Node, bool) | يستورد عقدة من وثيقة أخرى إلى الوثيقة الحالية. |
| [ImportNode](../../aspose.words/documentbase/importnode)(Node, bool, ImportFormatMode) | يستورد عقدة من وثيقة أخرى إلى الوثيقة الحالية مع خيار للتحكم في التنسيق. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | إرجاع فهرس العقدة الفرعية المحددة في مصفوفة العقدة الفرعية. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | يدخل العقدة المحددة مباشرة بعد العقدة المرجعية المحددة. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | يقوم بإدراج العقدة المحددة مباشرة قبل العقدة المرجعية المحددة. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | الحصول على العقدة التالية وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | يضيف العقدة المحددة إلى بداية قائمة العقد الفرعية لهذه العقدة . |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق. |
| [Remove](../../aspose.words/node/remove)() | يزيل نفسه من الأصل. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | يزيل كافة العقد التابعة للعقدة الحالية. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | يزيل العقدة الفرعية المحددة . |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | يزيل الكل[`SmartTag`](../../aspose.words.markup/smarttag) العقد التابعة للعقدة الحالية. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | تحديد قائمة بالعقد المطابقة لتعبير XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | تحديد العقدة الأولى التي تطابق تعبير XPath. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | يصدر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

### ملاحظات

يمكن أن تحتوي بعض المستندات ، عادةً قوالب ، على نص تلقائي وإدخالات التصحيح التلقائي_ x000d_ و / أو كتل الإنشاء (تُعرف أيضًا باسمإدخالات وثيقة مسرد وأجزاء الوثيقة أواللبنات).

للوصول إلى الكتل البرمجية الإنشائية ، تحتاج إلى تحميل مستند إلى ملف[`Document`](../../aspose.words/document) كائن. اللبنات الأساسية ستكون متاحة عبر[`GlossaryDocument`](../../aspose.words/document/glossarydocument) منشأه.

[`GlossaryDocument`](../glossarydocument) يمكن أن تحتوي على أي عدد من[`BuildingBlock`](../buildingblock) الكائنات ._ x000d_ لكل منهما[`BuildingBlock`](../buildingblock) يمثل جزءًا واحدًا من المستند.

يتوافق مع **وثيقة** و **docParts**العناصر في OOXML.

### أمثلة

يعرض طرق الوصول إلى الكتل البرمجية الإنشائية في مستند مسرد.

```csharp
public void GlossaryDocument()
{
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();

    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 1" });
    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 2" });
    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 3" });
    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 4" });
    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 5" });

    Assert.AreEqual(5, glossaryDoc.BuildingBlocks.Count);

    doc.GlossaryDocument = glossaryDoc;

    // هناك طرق مختلفة للوصول إلى اللبنات الأساسية.
    // 1 - احصل على اللبنات الأساسية الأولى / الأخيرة في المجموعة:
    Assert.AreEqual("Block 1", glossaryDoc.FirstBuildingBlock.Name);
    Assert.AreEqual("Block 5", glossaryDoc.LastBuildingBlock.Name);

    // 2 - احصل على قالب بناء حسب الفهرس:
    Assert.AreEqual("Block 2", glossaryDoc.BuildingBlocks[1].Name);
    Assert.AreEqual("Block 3", glossaryDoc.BuildingBlocks.ToArray()[2].Name);

    // 3 - احصل على أول قالب إنشائي يطابق معرضًا واسمًا وفئة:
    Assert.AreEqual("Block 4", 
        glossaryDoc.GetBuildingBlock(BuildingBlockGallery.All, "(Empty Category)", "Block 4").Name);

    // سنفعل ذلك باستخدام زائر مخصص ،
    // الذي سيعطي كل BuildingBlock في GlossaryDocument GUID فريدًا
    GlossaryDocVisitor visitor = new GlossaryDocVisitor();
    glossaryDoc.Accept(visitor);

    Console.WriteLine(visitor.GetText());

    // في Microsoft Word ، يمكننا الوصول إلى اللبنات الأساسية عبر "إدراج" - > "أجزاء سريعة" - >. "منظم كتل البناء".
    doc.Save(ArtifactsDir + "BuildingBlocks.GlossaryDocument.dotx"); 
}

/// <summary>
/// يعطي كل كتلة إنشائية في مستند قاموس المصطلحات الذي تمت زيارته GUID فريدًا.
/// يخزن أزواج الكتل البرمجية الإنشائية GUID في قاموس.
/// </summary>
public class GlossaryDocVisitor : DocumentVisitor
{
    public GlossaryDocVisitor()
    {
        mBlocksByGuid = new Dictionary<Guid, BuildingBlock>();
        mBuilder = new StringBuilder();
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    public Dictionary<Guid, BuildingBlock> GetDictionary()
    {
        return mBlocksByGuid;
    }

    public override VisitorAction VisitGlossaryDocumentStart(GlossaryDocument glossary)
    {
        mBuilder.AppendLine("Glossary document found!");
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitGlossaryDocumentEnd(GlossaryDocument glossary)
    {
        mBuilder.AppendLine("Reached end of glossary!");
        mBuilder.AppendLine("BuildingBlocks found: " + mBlocksByGuid.Count);
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitBuildingBlockStart(BuildingBlock block)
    {
        block.Guid = Guid.NewGuid();
        mBlocksByGuid.Add(block.Guid, block);
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitBuildingBlockEnd(BuildingBlock block)
    {
        mBuilder.AppendLine("\tVisited block \"" + block.Name + "\"");
        mBuilder.AppendLine("\t Type: " + block.Type);
        mBuilder.AppendLine("\t Gallery: " + block.Gallery);
        mBuilder.AppendLine("\t Behavior: " + block.Behavior);
        mBuilder.AppendLine("\t Description: " + block.Description);

        return VisitorAction.Continue;
    }

    private readonly Dictionary<Guid, BuildingBlock> mBlocksByGuid;
    private readonly StringBuilder mBuilder;
}
```

### أنظر أيضا

* class [DocumentBase](../../aspose.words/documentbase)
* مساحة الاسم [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
