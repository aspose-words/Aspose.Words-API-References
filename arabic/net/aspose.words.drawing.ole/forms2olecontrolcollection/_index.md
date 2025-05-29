---
title: Forms2OleControlCollection Class
linktitle: Forms2OleControlCollection
articleTitle: Forms2OleControlCollection
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Drawing.Ole.Forms2OleControlCollection، الحل الخاص بك لإدارة كائنات Forms2OleControl بكفاءة في معالجة المستندات.
type: docs
weight: 1470
url: /ar/net/aspose.words.drawing.ole/forms2olecontrolcollection/
---
## Forms2OleControlCollection class

يمثل مجموعة من[`Forms2OleControl`](../forms2olecontrol/) الأشياء.

لمعرفة المزيد، قم بزيارة[العمل مع كائنات Ole](https://docs.aspose.com/words/net/working-with-ole-objects/) مقالة توثيقية.

```csharp
public class Forms2OleControlCollection : IEnumerable<Forms2OleControl>
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [Forms2OleControlCollection](forms2olecontrolcollection/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.drawing.ole/forms2olecontrolcollection/count/) { get; } | يحصل على عدد الكائنات في المجموعة. |
| [Item](../../aspose.words.drawing.ole/forms2olecontrolcollection/item/) { get; } | يحصل[`Forms2OleControl`](../forms2olecontrol/) الكائن عند فهرس محدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.ole/forms2olecontrolcollection/getenumerator/)() | يحصل على المُعدِّد. |

## أمثلة

يوضح كيفية الوصول إلى عنصر تحكم OLE المضمن في مستند وعناصر التحكم الفرعية الخاصة به.

```csharp
Document doc = new Document(MyDir + "OLE ActiveX controls.docm");

// تقوم الأشكال بتخزين وعرض كائنات OLE في نص المستند.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual("6e182020-f460-11ce-9bcd-00aa00608e01", shape.OleFormat.Clsid.ToString());

Forms2OleControl oleControl = (Forms2OleControl)shape.OleFormat.OleControl;

// قد تحتوي بعض عناصر تحكم OLE على عناصر تحكم فرعية، مثل تلك الموجودة في هذه الوثيقة والتي تحتوي على ثلاثة أزرار خيارات.
Forms2OleControlCollection oleControlCollection = oleControl.ChildNodes;

Assert.AreEqual(3, oleControlCollection.Count);

Assert.AreEqual("C#", oleControlCollection[0].Caption);
Assert.AreEqual("1", oleControlCollection[0].Value);

Assert.AreEqual("Visual Basic", oleControlCollection[1].Caption);
Assert.AreEqual("0", oleControlCollection[1].Value);

Assert.AreEqual("Delphi", oleControlCollection[2].Caption);
Assert.AreEqual("0", oleControlCollection[2].Value);
```

### أنظر أيضا

* class [Forms2OleControl](../forms2olecontrol/)
* مساحة الاسم [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* المجسم [Aspose.Words](../../)
