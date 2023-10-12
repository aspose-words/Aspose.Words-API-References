---
title: Enum WebExtensionBindingType
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.WebExtensions.WebExtensionBindingType تعداد. تعداد أنواع الارتباط المتاحة بين امتداد الويب والبيانات الموجودة في المستند.
type: docs
weight: 6770
url: /ar/net/aspose.words.webextensions/webextensionbindingtype/
---
## WebExtensionBindingType enumeration

تعداد أنواع الارتباط المتاحة بين امتداد الويب والبيانات الموجودة في المستند.

```csharp
public enum WebExtensionBindingType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Matrix | `0` | بيانات جدولية بدون صف رأس. |
| Table | `1` | بيانات جدولية تحتوي على صف رأس. |
| Text | `2` | نص عادي. |
| Default | `0` |  |

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


