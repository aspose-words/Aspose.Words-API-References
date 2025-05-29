---
title: TaskPane Class
linktitle: TaskPane
articleTitle: TaskPane
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.WebExtensions.TaskPane، وهي مفتاحك لإنشاء أجزاء مهام إضافية قوية لتحسين تحرير المستندات والإنتاجية.
type: docs
weight: 7560
url: /ar/net/aspose.words.webextensions/taskpane/
---
## TaskPane class

يمثل كائن جزء المهام الإضافية.

لمعرفة المزيد، قم بزيارة[العمل مع الوظائف الإضافية لـ Office](https://docs.aspose.com/words/net/work-with-office-add-ins/) مقالة توثيقية.

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
| [DockState](../../aspose.words.webextensions/taskpane/dockstate/) { get; set; } | يحدد آخر موقع تم فيه إرساء كائن جزء المهام هذا. |
| [IsLocked](../../aspose.words.webextensions/taskpane/islocked/) { get; set; } | يحدد ما إذا كان جزء المهام مقفلاً على المستند في واجهة المستخدم ولا يمكن للمستخدم إغلاقه. |
| [IsVisible](../../aspose.words.webextensions/taskpane/isvisible/) { get; set; } | يحدد ما إذا كان جزء المهام يظهر بشكل مرئي افتراضيًا عند فتح المستند. |
| [Row](../../aspose.words.webextensions/taskpane/row/) { get; set; } | يحدد الفهرس، من الخارج إلى الداخل، لجزء المهام هذا بين أجزاء المهام الأخرى الثابتة الموجودة في نفس الموقع الافتراضي. |
| [WebExtension](../../aspose.words.webextensions/taskpane/webextension/) { get; } | يمثل كائن امتداد الويب. |
| [Width](../../aspose.words.webextensions/taskpane/width/) { get; set; } | يحدد قيمة العرض الافتراضية لنسخة جزء المهام هذه. |

## أمثلة

يوضح كيفية إضافة ملحق ويب إلى مستند.

```csharp
Document doc = new Document();

// إنشاء جزء مهام باستخدام الوظيفة الإضافية "MyScript"، والتي سيتم استخدامها بواسطة المستند،
// ثم قم بتعيين موقعه الافتراضي.
TaskPane myScriptTaskPane = new TaskPane();
doc.WebExtensionTaskPanes.Add(myScriptTaskPane);
myScriptTaskPane.DockState = TaskPaneDockState.Right;
myScriptTaskPane.IsVisible = true;
myScriptTaskPane.Width = 300;
myScriptTaskPane.IsLocked = true;

// إذا كان هناك أجزاء مهام متعددة في نفس موقع الإرساء، فيمكننا تعيين هذا الفهرس لترتيبها.
myScriptTaskPane.Row = 1;

// قم بإنشاء وظيفة إضافية تسمى "MyScript Math Sample"، والتي سيتم عرض جزء المهام بداخلها.
WebExtension webExtension = myScriptTaskPane.WebExtension;

// تعيين معلمات مرجع متجر التطبيقات للوظيفة الإضافية الخاصة بنا، مثل المعرف.
webExtension.Reference.Id = "WA104380646";
webExtension.Reference.Version = "1.0.0.0";
webExtension.Reference.StoreType = WebExtensionStoreType.OMEX;
webExtension.Reference.Store = CultureInfo.CurrentCulture.Name;
webExtension.Properties.Add(new WebExtensionProperty("MyScript", "MyScript Math Sample"));
webExtension.Bindings.Add(new WebExtensionBinding("MyScript", WebExtensionBindingType.Text, "104380646"));

//السماح للمستخدم بالتفاعل مع الوظيفة الإضافية.
webExtension.IsFrozen = false;

// يمكننا الوصول إلى ملحق الويب في Microsoft Word عبر Developer -> Add-ins.
doc.Save(ArtifactsDir + "Document.WebExtension.docx");

// قم بإزالة جميع أجزاء مهام ملحق الويب مرة واحدة مثل هذا.
doc.WebExtensionTaskPanes.Clear();

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);

doc = new Document(ArtifactsDir + "Document.WebExtension.docx");

myScriptTaskPane = doc.WebExtensionTaskPanes[0];
Assert.AreEqual(TaskPaneDockState.Right, myScriptTaskPane.DockState);
Assert.True(myScriptTaskPane.IsVisible);
Assert.AreEqual(300.0d, myScriptTaskPane.Width);
Assert.True(myScriptTaskPane.IsLocked);
Assert.AreEqual(1, myScriptTaskPane.Row);

webExtension = myScriptTaskPane.WebExtension;
Assert.AreEqual(string.Empty, webExtension.Id);

Assert.AreEqual("WA104380646", webExtension.Reference.Id);
Assert.AreEqual("1.0.0.0", webExtension.Reference.Version);
Assert.AreEqual(WebExtensionStoreType.OMEX, webExtension.Reference.StoreType);
Assert.AreEqual(CultureInfo.CurrentCulture.Name, webExtension.Reference.Store);
Assert.AreEqual(0, webExtension.AlternateReferences.Count);

Assert.AreEqual("MyScript", webExtension.Properties[0].Name);
Assert.AreEqual("MyScript Math Sample", webExtension.Properties[0].Value);

Assert.AreEqual("MyScript", webExtension.Bindings[0].Id);
Assert.AreEqual(WebExtensionBindingType.Text, webExtension.Bindings[0].BindingType);
Assert.AreEqual("104380646", webExtension.Bindings[0].AppRef);

Assert.False(webExtension.IsFrozen);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* المجسم [Aspose.Words](../../)
