---
title: WebExtensionStoreType Enum
linktitle: WebExtensionStoreType
articleTitle: WebExtensionStoreType
second_title: Aspose.Words لـ .NET
description: اكتشف مجموعة Aspose.Words.WebExtensionStoreType، التي تتميز بأنواع مختلفة من متاجر ملحقات الويب لتحقيق التكامل السلس والوظائف المحسنة.
type: docs
weight: 7670
url: /ar/net/aspose.words.webextensions/webextensionstoretype/
---
## WebExtensionStoreType enumeration

يقوم بإحصاء الأنواع المتوفرة لمتجر ملحقات الويب.

```csharp
public enum WebExtensionStoreType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| SPCatalog | `0` | يحدد أن نوع المتجر هو كتالوج SharePoint المؤسسي. |
| OMEX | `1` | يحدد أن نوع المتجر هو Office.com. |
| SPApp | `2` | يحدد أن نوع المتجر هو تطبيق ويب SharePoint. |
| Exchange | `3` | يحدد أن نوع المتجر هو خادم Exchange. |
| FileSystem | `4` | يحدد أن نوع المتجر هو مشاركة نظام الملفات. |
| Registry | `5` | يحدد أن نوع المتجر هو سجل النظام. |
| ExCatalog | `6` | يحدد أن نوع المتجر هو النشر المركزي عبر Exchange. |
| Default | `0` | القيمة الافتراضية. |

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
