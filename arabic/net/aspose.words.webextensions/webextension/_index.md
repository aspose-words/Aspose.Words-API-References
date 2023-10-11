---
title: Class WebExtension
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.WebExtensions.WebExtension فصل. يمثل كائن ملحق الويب.
type: docs
weight: 6740
url: /ar/net/aspose.words.webextensions/webextension/
---
## WebExtension class

يمثل كائن ملحق الويب.

لمعرفة المزيد، قم بزيارة[العمل مع وظائف Office الإضافية](https://docs.aspose.com/words/net/work-with-office-add-ins/) مقالة توثيقية.

```csharp
public class WebExtension
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [AlternateReferences](../../aspose.words.webextensions/webextension/alternatereferences/) { get; } | يحدد مراجع بديلة لامتداد الويب. |
| [Bindings](../../aspose.words.webextensions/webextension/bindings/) { get; } | يحدد قائمة روابط امتدادات الويب. |
| [Id](../../aspose.words.webextensions/webextension/id/) { get; set; } | يحدد بشكل فريد مثيل ملحق الويب في المستند الحالي. |
| [IsFrozen](../../aspose.words.webextensions/webextension/isfrozen/) { get; set; } | يحدد ما إذا كان يمكن للمستخدم التفاعل مع ملحق الويب أم لا. |
| [Properties](../../aspose.words.webextensions/webextension/properties/) { get; } | يمثل مجموعة من الخصائص المخصصة لامتداد الويب. |
| [Reference](../../aspose.words.webextensions/webextension/reference/) { get; } | يحدد المرجع الأساسي لامتداد الويب. |

### أمثلة

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


