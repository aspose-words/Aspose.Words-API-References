---
title: GlossaryDocument Class
linktitle: GlossaryDocument
articleTitle: GlossaryDocument
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.BuildingBlocks.GlossaryDocument، وهي مفتاحك لإدارة AutoText وBuilding Blocks بسلاسة في مستندات Word.
type: docs
weight: 370
url: /ar/net/aspose.words.buildingblocks/glossarydocument/
---
## GlossaryDocument class

يمثل العنصر الجذر لمستند المصطلحات داخل مستند Word. مستند المصطلحات هو مخزن للنص التلقائي وإدخالات التصحيح التلقائي وكتل البناء.

لمعرفة المزيد، قم بزيارة[نموذج كائن المستند (DOM) في Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) مقالة توثيقية.

```csharp
public class GlossaryDocument : DocumentBase
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [GlossaryDocument](glossarydocument/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape/) { get; set; } | يحصل على شكل خلفية المستند أو يضبطه. يمكن استخدامه`باطل` . |
| [BuildingBlocks](../../aspose.words.buildingblocks/glossarydocument/buildingblocks/) { get; } | يعيد مجموعة مكتوبة تمثل جميع كتل البناء في مستند المصطلحات. |
| [Count](../../aspose.words/compositenode/count/) { get; } | يحصل على عدد الأبناء المباشرين لهذه العقدة. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصص. |
| override [Document](../../aspose.words/documentbase/document/) { get; } | يحصل على هذه المثيل. |
| [FirstBuildingBlock](../../aspose.words.buildingblocks/glossarydocument/firstbuildingblock/) { get; } | يحصل على كتلة البناء الأولى في مستند المصطلحات. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | يحصل على أول طفل للعقدة. |
| [FontInfos](../../aspose.words/documentbase/fontinfos/) { get; } | يوفر الوصول إلى خصائص الخطوط المستخدمة في هذه الوثيقة. |
| [FootnoteSeparators](../../aspose.words/documentbase/footnoteseparators/) { get; } | يوفر الوصول إلى فواصل الحواشي السفلية/النهائية المحددة في المستند. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | إرجاع`حقيقي` حيث يمكن لهذه العقدة أن تحتوي على عقد فرعية. |
| [LastBuildingBlock](../../aspose.words.buildingblocks/glossarydocument/lastbuildingblock/) { get; } | يحصل على آخر كتلة بناء في مستند المصطلحات. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | يحصل على آخر طفل للعقدة. |
| [Lists](../../aspose.words/documentbase/lists/) { get; } | يوفر الوصول إلى تنسيق القائمة المستخدم في المستند. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback/) { get; set; } | يتم استدعاؤها عند إدراج عقدة أو إزالتها في المستند. |
| override [NodeType](../../aspose.words.buildingblocks/glossarydocument/nodetype/) { get; } | يعيدGlossaryDocument القيمة. |
| [PageColor](../../aspose.words/documentbase/pagecolor/) { get; set; } | يُحدِّد لون صفحة المستند أو يُحدِّده. هذه الخاصية هي نسخة أبسط من[`BackgroundShape`](../../aspose.words/documentbase/backgroundshape/) . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الوالد المباشر لهذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [Range](../../aspose.words/node/range/) { get; } | يعيد[`Range`](../../aspose.words/range/)الكائن الذي يمثل الجزء من المستند الموجود في هذه العقدة. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback/) { get; set; } | يسمح بالتحكم في كيفية تحميل الموارد الخارجية. |
| [Styles](../../aspose.words/documentbase/styles/) { get; } | يعيد مجموعة من الأنماط المحددة في المستند. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback/) { get; set; } | يتم استدعاؤها أثناء إجراءات معالجة المستندات المختلفة عند اكتشاف مشكلة قد تؤدي إلى فقدان دقة البيانات أو التنسيق. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words.buildingblocks/glossarydocument/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | يقبل زائرًا. |
| override [AcceptEnd](../../aspose.words.buildingblocks/glossarydocument/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | يقبل الزائر لزيارة نهاية مستند المصطلحات. |
| override [AcceptStart](../../aspose.words.buildingblocks/glossarydocument/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | يقبل الزائر لزيارة بداية مستند المصطلحات. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | يضيف العقدة المحددة إلى نهاية قائمة العقد الفرعية لهذه العقدة. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | ينشئ نسخة مكررة من العقدة. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | ينشئ متصفحًا يمكن استخدامه للتنقل بين العقد وقراءتها. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | يحصل على السلف الأول للعنصر المحدد[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | يحصل على السلف الأول لنوع الكائن المحدد. |
| [GetBuildingBlock](../../aspose.words.buildingblocks/glossarydocument/getbuildingblock/)(*[BuildingBlockGallery](../buildingblockgallery/), string, string*) | يبحث عن كتلة بناء باستخدام المعرض والفئة والاسم المحددين. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | يعيد عقدة فرعية رقم N تطابق النوع المحدد. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | يعيد مجموعة حية من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | يوفر الدعم لكل تكرار للأسلوب على العقد الفرعية لهذه العقدة. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | يحصل على نص هذه العقدة وجميع أبنائها. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(*[Node](../../aspose.words/node/), bool*) | استيراد عقدة من مستند آخر إلى المستند الحالي. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(*[Node](../../aspose.words/node/), bool, [ImportFormatMode](../../aspose.words/importformatmode/)*) | استيراد عقدة من مستند آخر إلى المستند الحالي مع خيار التحكم في التنسيق. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | يعيد مؤشر العقدة الفرعية المحددة في مجموعة العقد الفرعية. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | يقوم بإدراج العقدة المحددة فورًا بعد عقدة المرجع المحددة. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | يقوم بإدراج العقدة المحددة مباشرة قبل عقدة المرجع المحددة. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | يحصل على العقدة التالية وفقًا لخوارزمية عبور شجرة الترتيب المسبق. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | يضيف العقدة المحددة إلى بداية قائمة العقد الفرعية لهذه العقدة. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | يحصل على العقدة السابقة وفقًا لخوارزمية عبور شجرة الترتيب المسبق. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | يزيل جميع العقد الفرعية للعقدة الحالية. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | يزيل العقدة الفرعية المحددة. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | يزيل الكل[`SmartTag`](../../aspose.words.markup/smarttag/) العقد المنحدرة من العقدة الحالية. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | يحدد قائمة العقد المطابقة لتعبير XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | يحدد الأول[`Node`](../../aspose.words/node/) الذي يتطابق مع تعبير XPath. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | يقوم بتصدير محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

## ملاحظات

يمكن أن تحتوي بعض المستندات، عادةً القوالب، على نص تلقائي وإدخالات التصحيح التلقائي و/أو كتل البناء (المعروفة أيضًا باسممدخلات وثيقة المصطلحات ،أجزاء الوثيقة أوكتل البناء).

للوصول إلى كتل البناء، تحتاج إلى تحميل مستند في[`Document`](../../aspose.words/document/) كائن . ستكون كتل البناء متاحة عبر[`GlossaryDocument`](../../aspose.words/document/glossarydocument/) ملكية.

`GlossaryDocument` يمكن أن تحتوي على أي عدد من[`BuildingBlock`](../buildingblock/)الكائنات. لكل[`BuildingBlock`](../buildingblock/) يمثل جزء واحد من الوثيقة.

يتوافق مع**مسرد المصطلحات** و**أجزاء المستندات**العناصر في OOXML.

## أمثلة

يوضح طرق الوصول إلى كتل البناء في مستند المصطلحات.

```csharp
public void GlossaryDocument()
{
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();

    BuildingBlock child1 = new BuildingBlock(glossaryDoc) { Name = "Block 1" };
    glossaryDoc.AppendChild(child1);
    BuildingBlock child2 = new BuildingBlock(glossaryDoc) { Name = "Block 2" };
    glossaryDoc.AppendChild(child2);
    BuildingBlock child3 = new BuildingBlock(glossaryDoc) { Name = "Block 3" };
    glossaryDoc.AppendChild(child3);
    BuildingBlock child4 = new BuildingBlock(glossaryDoc) { Name = "Block 4" };
    glossaryDoc.AppendChild(child4);
    BuildingBlock child5 = new BuildingBlock(glossaryDoc) { Name = "Block 5" };
    glossaryDoc.AppendChild(child5);

    Assert.AreEqual(5, glossaryDoc.BuildingBlocks.Count);

    doc.GlossaryDocument = glossaryDoc;

    // هناك طرق مختلفة للوصول إلى كتل البناء.
    // 1 - احصل على أول/آخر كتلة بناء في المجموعة:
    Assert.AreEqual("Block 1", glossaryDoc.FirstBuildingBlock.Name);
    Assert.AreEqual("Block 5", glossaryDoc.LastBuildingBlock.Name);

    // 2 - الحصول على كتلة بناء حسب الفهرس:
    Assert.AreEqual("Block 2", glossaryDoc.BuildingBlocks[1].Name);
    Assert.AreEqual("Block 3", glossaryDoc.BuildingBlocks.ToArray()[2].Name);

    // 3 - احصل على أول كتلة بناء تتطابق مع المعرض والاسم والفئة:
    Assert.AreEqual("Block 4", 
        glossaryDoc.GetBuildingBlock(BuildingBlockGallery.All, "(Empty Category)", "Block 4").Name);

    // سوف نفعل ذلك باستخدام زائر مخصص،
    // مما سيعطي لكل BuildingBlock في GlossaryDocument معرف GUID فريدًا
    GlossaryDocVisitor visitor = new GlossaryDocVisitor();
    // قم بزيارة بداية/نهاية مستند المصطلحات.
    glossaryDoc.Accept(visitor);
    // قم بزيارة بداية مستند المصطلحات فقط.
    glossaryDoc.AcceptStart(visitor);
    // قم بزيارة نهاية مستند المصطلحات فقط.
    glossaryDoc.AcceptEnd(visitor);
    Console.WriteLine(visitor.GetText());

    // في Microsoft Word، يمكننا الوصول إلى كتل البناء عبر "إدراج" -> "الأجزاء السريعة" -> "منظم كتل البناء".
    doc.Save(ArtifactsDir + "BuildingBlocks.GlossaryDocument.dotx"); 
}

/// <summary>
/// يمنح كل كتلة بناء في مستند المصطلحات الذي تمت زيارتها معرف GUID فريدًا.
/// يخزن أزواج كتلة بناء GUID في القاموس.
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

* class [DocumentBase](../../aspose.words/documentbase/)
* مساحة الاسم [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks/)
* المجسم [Aspose.Words](../../)
