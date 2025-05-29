---
title: Forms2OleControlType Enum
linktitle: Forms2OleControlType
articleTitle: Forms2OleControlType
second_title: Aspose.Words لـ .NET
description: اكتشف مجموعة Aspose.Words.Drawing.Ole.Forms2OleControlType، التي تتميز بمجموعة من أنواع عناصر التحكم في Forms 2.0 لتحسين أتمتة المستندات.
type: docs
weight: 1480
url: /ar/net/aspose.words.drawing.ole/forms2olecontroltype/
---
## Forms2OleControlType enumeration

يقوم بإحصاء أنواع عناصر التحكم في Forms 2.0.

```csharp
public enum Forms2OleControlType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| OptionButton | `0` | عنصر تحكم زر الراديو. |
| Label | `1` | عنصر تحكم يعرض النص. |
| Textbox | `2` | عنصر تحكم يسمح للمستخدم بإدخال النص. |
| CheckBox | `3` | عنصر تحكم يسمح للمستخدم بتحديد خيار أو إلغاء تحديده. |
| ToggleButton | `4` | عنصر تحكم يسمح للمستخدم بالتبديل بين حالتين. |
| SpinButton | `5` | عنصر تحكم يسمح للمستخدم بزيادة أو تقليل القيمة. |
| ComboBox | `6` | عنصر تحكم يسمح للمستخدم باختيار عنصر من القائمة. |
| Frame | `7` | عنصر تحكم يجمع عناصر التحكم الأخرى. |
| MultiPage | `8` | عنصر تحكم يعرض صفحات متعددة من المحتوى. |
| TabStrip | `9` | عنصر تحكم يسمح للمستخدم بالتبديل بين صفحات متعددة من المحتوى. |
| CommandButton | `10` | زر يؤدي إلى تنفيذ إجراء عند النقر عليه. |
| Image | `11` | عنصر تحكم يعرض صورة. |
| ScrollBar | `12` | عنصر تحكم يسمح للمستخدم بالتمرير عبر المحتوى. |
| Form | `13` | حاوية لعناصر التحكم الأخرى. |
| ListBox | `14` | عنصر تحكم يعرض قائمة من العناصر. |

## أمثلة

يوضح كيفية تغيير حالة عنصر التحكم CheckBox.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
CheckBoxControl checkBoxControl = (CheckBoxControl)shape.OleFormat.OleControl;
checkBoxControl.Checked = true;

Assert.AreEqual(true, checkBoxControl.Checked);
Assert.AreEqual(Forms2OleControlType.CheckBox, checkBoxControl.Type);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* المجسم [Aspose.Words](../../)
