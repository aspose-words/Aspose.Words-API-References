---
title: TaskPane Class
linktitle: TaskPane
articleTitle: TaskPane
second_title: Aspose.Words لـ .NET
description: Aspose.Words.WebExtensions.TaskPane فصل. يمثل كائن جزء المهام الإضافي في C#.
type: docs
weight: 6710
url: /ar/net/aspose.words.webextensions/taskpane/
---
## TaskPane class

يمثل كائن جزء المهام الإضافي.

لمعرفة المزيد، قم بزيارة[العمل مع وظائف Office الإضافية](https://docs.aspose.com/words/net/work-with-office-add-ins/) مقالة توثيقية.

```csharp
public class TaskPane
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [TaskPane](taskpane/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [DockState](../../aspose.words.webextensions/taskpane/dockstate/) { get; set; } | يحدد الموقع الأخير لكائن جزء المهام هذا. |
| [IsLocked](../../aspose.words.webextensions/taskpane/islocked/) { get; set; } | يحدد ما إذا كان جزء المهام مقفلاً على المستند في واجهة المستخدم ولا يمكن للمستخدم إغلاقه. |
| [IsVisible](../../aspose.words.webextensions/taskpane/isvisible/) { get; set; } | يحدد ما إذا كان جزء المهام يظهر بشكل افتراضي عند فتح المستند. |
| [Row](../../aspose.words.webextensions/taskpane/row/) { get; set; } | يحدد الفهرس، الذي يعدد من الخارج إلى الداخل، لجزء المهام هذا من بين أجزاء المهام المستمرة المثبتة في نفس الموقع الافتراضي. |
| [WebExtension](../../aspose.words.webextensions/taskpane/webextension/) { get; } | يمثل كائن ملحق الويب. |
| [Width](../../aspose.words.webextensions/taskpane/width/) { get; set; } | يحدد قيمة العرض الافتراضية لمثيل جزء المهام هذا. |

## أمثلة

يوضح كيفية إضافة ملحق ويب إلى مستند.

```csharp
Document doc = new Document();

// قم بإنشاء جزء المهام باستخدام الوظيفة الإضافية "MyScript"، والتي سيتم استخدامها بواسطة المستند،
// ثم قم بتعيين موقعه الافتراضي.
TaskPane myScriptTaskPane = new TaskPane();
doc.WebExtensionTaskPanes.Add(myScriptTaskPane);
myScriptTaskPane.DockState = TaskPaneDockState.Right;
myScriptTaskPane.IsVisible = true;
myScriptTaskPane.Width = 300;
myScriptTaskPane.IsLocked = true;

// إذا كانت هناك أجزاء مهام متعددة في نفس موقع الإرساء، فيمكننا ضبط هذا الفهرس لترتيبها.
myScriptTaskPane.Row = 1;

// قم بإنشاء وظيفة إضافية تسمى "MyScript Math Sample"، والتي سيعرضها جزء المهام بداخلها.
WebExtension webExtension = myScriptTaskPane.WebExtension;

// قم بتعيين المعلمات المرجعية لمتجر التطبيقات للوظيفة الإضافية لدينا، مثل المعرف.
webExtension.Reference.Id = "WA104380646";
webExtension.Reference.Version = "1.0.0.0";
webExtension.Reference.StoreType = WebExtensionStoreType.OMEX;
webExtension.Reference.Store = CultureInfo.CurrentCulture.Name;
webExtension.Properties.Add(new WebExtensionProperty("MyScript", "MyScript Math Sample"));
webExtension.Bindings.Add(new WebExtensionBinding("MyScript", WebExtensionBindingType.Text, "104380646"));

// السماح للمستخدم بالتفاعل مع الوظيفة الإضافية.
webExtension.IsFrozen = false;

// يمكننا الوصول إلى ملحق الويب في Microsoft Word عبر المطور -> الوظائف الإضافية.
doc.Save(ArtifactsDir + "Document.WebExtension.docx");

// قم بإزالة كافة أجزاء المهام الخاصة بامتداد الويب مرة واحدة بهذه الطريقة.
doc.WebExtensionTaskPanes.Clear();

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* المجسم [Aspose.Words](../../)
