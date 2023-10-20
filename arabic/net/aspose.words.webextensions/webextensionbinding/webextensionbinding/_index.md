---
title: WebExtensionBinding
linktitle: WebExtensionBinding
articleTitle: WebExtensionBinding
second_title: Aspose.Words لـ .NET
description: WebExtensionBinding البناء. ينشئ ربط ملحق الويب بمعلمات محددة في C#.
type: docs
weight: 10
url: /ar/net/aspose.words.webextensions/webextensionbinding/webextensionbinding/
---
## WebExtensionBinding constructor

ينشئ ربط ملحق الويب بمعلمات محددة.

```csharp
public WebExtensionBinding(string id, WebExtensionBindingType bindingType, string appRef)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| id | String | معرف ملزم. |
| bindingType | WebExtensionBindingType | نوع ملزمة. |
| appRef | String | مفتاح الربط المستخدم لتعيين إدخال الربط في هذه القائمة مع البيانات المرتبطة في المستند. |

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

* enum [WebExtensionBindingType](../../webextensionbindingtype/)
* class [WebExtensionBinding](../)
* مساحة الاسم [Aspose.Words.WebExtensions](../../../aspose.words.webextensions/)
* المجسم [Aspose.Words](../../../)
