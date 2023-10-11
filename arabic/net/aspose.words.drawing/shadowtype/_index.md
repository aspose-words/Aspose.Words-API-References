---
title: Enum ShadowType
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Drawing.ShadowType تعداد. يحدد نوع ظل الشكل.
type: docs
weight: 1240
url: /ar/net/aspose.words.drawing/shadowtype/
---
## ShadowType enumeration

يحدد نوع ظل الشكل.

```csharp
public enum ShadowType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| ShadowMixed | `-2` | لا يوجد أي من إعدادات الظل المحددة مسبقًا. |
| Shadow1 | `1` | نوع الظل الأول. |
| Shadow10 | `10` | نوع الظل العاشر. |
| Shadow11 | `11` | نوع الظل الحادي عشر. |
| Shadow12 | `12` | نوع الظل الثاني عشر. |
| Shadow13 | `13` | نوع الظل الثالث عشر. |
| Shadow14 | `14` | نوع الظل الرابع عشر. |
| Shadow15 | `15` | نوع الظل الخامس عشر. |
| Shadow16 | `16` | نوع الظل السادس عشر. |
| Shadow17 | `17` | نوع الظل السابع عشر. |
| Shadow18 | `18` | نوع الظل الثامن عشر. |
| Shadow19 | `19` | نوع الظل التاسع عشر. |
| Shadow2 | `2` | نوع الظل الثاني. |
| Shadow20 | `20` | نوع الظل العشرين. |
| Shadow21 | `21` | نوع الظل الحادي والعشرون. |
| Shadow22 | `22` | نوع الظل الثاني والعشرون. |
| Shadow23 | `23` | نوع الظل الثالث والعشرون. |
| Shadow24 | `24` | نوع الظل الرابع والعشرون. |
| Shadow25 | `25` | نوع الظل الخامس والعشرون. |
| Shadow26 | `26` | نوع الظل السادس والعشرون. |
| Shadow27 | `27` | نوع الظل السابع والعشرون. |
| Shadow28 | `28` | نوع الظل الثامن والعشرون. |
| Shadow29 | `29` | نوع الظل التاسع والعشرون. |
| Shadow3 | `3` | نوع الظل الثالث. |
| Shadow30 | `30` | نوع الظل الثلاثون. |
| Shadow31 | `31` | نوع الظل الحادي والثلاثون. |
| Shadow32 | `32` | نوع الظل الثاني والثلاثون. |
| Shadow33 | `33` | نوع الظل الثالث والثلاثون. |
| Shadow34 | `34` | نوع الظل الرابع والثلاثون. |
| Shadow35 | `35` | نوع الظل الخامس والثلاثون. |
| Shadow36 | `36` | نوع الظل السادس والثلاثون. |
| Shadow37 | `37` | نوع الظل السابع والثلاثون. |
| Shadow38 | `38` | نوع الظل الثامن والثلاثون. |
| Shadow39 | `39` | نوع الظل التاسع والثلاثون. |
| Shadow4 | `4` | نوع الظل الرابع. |
| Shadow40 | `40` | نوع الظل الأربعون. |
| Shadow41 | `41` | نوع الظل الأول والأربعون. |
| Shadow42 | `42` | نوع الظل الثاني والأربعون. |
| Shadow43 | `43` | نوع الظل الثالث والأربعون. |
| Shadow5 | `5` | نوع الظل الخامس. |
| Shadow6 | `6` | نوع الظل السادس. |
| Shadow7 | `7` | نوع الظل السابع. |
| Shadow8 | `8` | نوع الظل الثامن. |
| Shadow9 | `9` | نوع الظل التاسع. |

### ملاحظات

ShadowType ليس سمة بسيطة، ولكنه إعداد مسبق يقوم بتعيين عدة سمات في وقت واحد والتي تشكل مظهر الظل .

### أمثلة

يوضح كيفية العمل مع تنسيق الظل للشكل.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];

if (shape.ShadowFormat.Visible && shape.ShadowFormat.Type == ShadowType.Shadow2)                
    shape.ShadowFormat.Type = ShadowType.Shadow7;

if (shape.ShadowFormat.Type == ShadowType.ShadowMixed)            
    shape.ShadowFormat.Clear();
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)


