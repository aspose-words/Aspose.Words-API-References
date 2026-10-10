---
title: "Aspose::Words::Drawing::ShapeType تعداد"
linktitle: "ShapeType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::ShapeType تعداد. يحدد نوع الشكل في مستند Microsoft Word في C++."
type: docs
weight: 38000
url: /ar/cpp/aspose.words.drawing/shapetype/
---
## ShapeType enum


يحدد نوع الشكل في مستند Microsoft Word.

```cpp
enum class ShapeType
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| Image | 75 | الشكل هو صورة. |
| مربع النص | 202 | الشكل هو مربع نص. لاحظ أن الأشكال من أنواع أخرى كثيرة يمكن أن تحتوي أيضًا على نص بداخلها. لا يلزم أن يكون الشكل من هذا النوع ليحتوي على نص. |
| مجموعة | -1 | الشكل هو شكل مجموعة. |
| OleObject | -2 | الشكل هو كائن OLE. لا يمكنك إنشاء أشكال من هذا النوع في المستند. |
| OleControl | 201 | الشكل هو عنصر تحكم ActiveX. لا يمكنك إنشاء أشكال من هذا النوع في المستند. |
| NonPrimitive | 0 | شكل يرسمه المستخدم ويتكون من عدة مقاطع و/أو رؤوس (منحنى، شكل حر أو خربشة). لا يمكنك إنشاء أشكال من هذا النوع في المستند. |
| Rectangle | 1 | مستطيل. |
| RoundRectangle | 2 | مستطيل مستدير. |
| Ellipse | 3 | بيضاوي. |
| Diamond | 4 | معين. |
| Triangle | 5 | مثلث. |
| RightTriangle | 6 | مثلث قائم. |
| Parallelogram | 7 | متوازي أضلاع. |
| Trapezoid | 8 | شبه منحرف. |
| Hexagon | 9 | سداسي. |
| Octagon | 10 | مثمن. |
| زائد | 11 | زائد. |
| نجمة | 12 | نجمة. |
| سهم | 13 | سهم. |
| سهم سميك | 14 | سهم سميك. |
| لوحة المنزل | 15 | لوحة المنزل. |
| مكعب | 16 | مكعب. |
| بالون | 17 | بالون. |
| ختم | 18 | ختم. |
| قوس | 19 | قوس. |
| خط | 20 | خط. |
| لوحة | 21 | لوحة. |
| علبة | 22 | علبة. |
| دونات | 23 | دونات. |
| TextSimple | 24 | نص بسيط. |
| TextOctagon | 25 | نص مثمن. |
| TextHexagon | 26 | نص سداسي. |
| TextCurve | 27 | نص منحني. |
| TextWave | 28 | نص موجة. |
| TextRing | 29 | نص حلقة. |
| TextOnCurve | 30 | نص على منحنى. |
| TextOnRing | 31 | نص على حلقة. |
| StraightConnector1 | 32 | شكل موصل مستقيم. |
| BentConnector2 | 33 | شكل موصل منحني مع مقطعين. |
| BentConnector3 | 34 | شكل موصل منحني مع ثلاثة مقاطع. |
| BentConnector4 | 35 | شكل موصل منحني مع أربعة مقاطع. |
| BentConnector5 | 36 | شكل موصل منحني بخمسة أقسام. |
| CurvedConnector2 | 37 | شكل موصل منحني باثنين من الأقسام. |
| CurvedConnector3 | 38 | شكل موصل منحني بثلاثة أقسام. |
| CurvedConnector4 | 39 | شكل موصل منحني بأربعة أقسام. |
| CurvedConnector5 | 40 | شكل موصل منحني بخمسة أقسام. |
| Callout1 | 41 | شكل ملاحظة بسهم واحد. |
| Callout2 | 42 | شكل ملاحظة بسهمين. |
| Callout3 | 43 | شكل ملاحظة بثلاثة أسهم. |
| AccentCallout1 | 44 | شكل ملاحظة مميزة بسهم واحد. |
| AccentCallout2 | 45 | شكل ملاحظة مميزة بسهمين. |
| AccentCallout3 | 46 | شكل ملاحظة مميزة بثلاثة أسهم. |
| BorderCallout1 | 47 | [Border](../../aspose.words/border/) ملاحظة 1. |
| BorderCallout2 | 48 | [Border](../../aspose.words/border/) ملاحظة 2. |
| BorderCallout3 | 49 | [Border](../../aspose.words/border/) ملاحظة 3. |
| AccentBorderCallout1 | 50 | نداء حدود مميزة 1. |
| AccentBorderCallout2 | 51 | نداء حدود مميزة 2. |
| AccentBorderCallout3 | 52 | نداء حدود مميزة 3. |
| Ribbon | 53 | شريط. |
| Ribbon2 | 54 | شريط 2. |
| Chevron | 55 | شيفرون. |
| Pentagon | 56 | خماسي. |
| NoSmoking | 57 | ممنوع التدخين. |
| Seal8 | 58 | نجمة ذات ثمانية نقاط. |
| Seal16 | 59 | نجمة ذات ستة عشر نقطة. |
| Seal32 | 60 | نجمة ذات اثنان وثلاثون نقطة. |
| WedgeRectCallout | 61 | نداء مستطيل إسفيني. |
| WedgeRRectCallout | 62 | ملاحظة Wedge R rect. |
| WedgeEllipseCallout | 63 | ملاحظة Wedge ellipse. |
| Wave | 64 | موجة. |
| FoldedCorner | 65 | زاوية مطوية. |
| LeftArrow | 66 | سهم إلى اليسار. |
| DownArrow | 67 | سهم إلى الأسفل. |
| UpArrow | 68 | سهم إلى الأعلى. |
| LeftRightArrow | 69 | سهم إلى اليسار واليمين. |
| UpDownArrow | 70 | سهم إلى الأعلى والأسفل. |
| IrregularSeal1 | 71 | ختم غير منتظم 1. |
| IrregularSeal2 | 72 | ختم غير منتظم 2. |
| LightningBolt | 73 | صاعقة. |
| Heart | 74 | قلب. |
| QuadArrow | 76 | سهم رباعي. |
| LeftArrowCallout | 77 | ملاحظة سهم إلى اليسار. |
| RightArrowCallout | 78 | ملاحظة سهم إلى اليمين. |
| UpArrowCallout | 79 | ملاحظة سهم إلى الأعلى. |
| DownArrowCallout | 80 | ملاحظة سهم إلى الأسفل. |
| LeftRightArrowCallout | 81 | ملاحظة سهم إلى اليسار واليمين. |
| UpDownArrowCallout | 82 | ملاحظة سهم إلى الأعلى والأسفل. |
| QuadArrowCallout | 83 | ملاحظة سهم رباعي. |
| منحدر | 84 | منحدر. |
| LeftBracket | 85 | قوس أيسر. |
| RightBracket | 86 | قوس أيمن. |
| LeftBrace | 87 | قوس معقوف أيسر. |
| RightBrace | 88 | قوس معقوف أيمن. |
| LeftUpArrow | 89 | سهم إلى اليسار أعلى. |
| BentUpArrow | 90 | سهم منحني أعلى. |
| BentArrow | 91 | سهم منحني. |
| Seal24 | 92 | نجمة ذات 24 نقطة. |
| StripedRightArrow | 93 | سهم يمين مخطط. |
| NotchedRightArrow | 94 | سهم يمين مسنن. |
| BlockArc | 95 | قوس كتلي. |
| SmileyFace | 96 | وجه مبتسم. |
| VerticalScroll | 97 | تمرير عمودي. |
| HorizontalScroll | 98 | تمرير أفقي. |
| CircularArrow | 99 | سهم دائري. |
| CustomShape | 100 | يبدو أن نوع الشكل هذا مخصص للأشكال التي لا تنتمي إلى مجموعة الأشكال التلقائية القياسية في Microsoft Word. على سبيل المثال، إذا قمت بإدراج شكل تلقائي جديد من ClipArt. لا يمكنك إنشاء أشكال من هذا النوع في المستند. |
| UturnArrow | 101 | سهم عكسي. |
| CurvedRightArrow | 102 | سهم منحني إلى اليمين. |
| CurvedLeftArrow | 103 | سهم منحني إلى اليسار. |
| CurvedUpArrow | 104 | سهم منحني إلى الأعلى. |
| CurvedDownArrow | 105 | سهم منحني إلى الأسفل. |
| CloudCallout | 106 | ملاحظة سحابية. |
| EllipseRibbon | 107 | شريط بيضاوي. |
| EllipseRibbon2 | 108 | شريط بيضاوي 2. |
| FlowChartProcess | 109 | عملية مخطط تدفق. |
| FlowChartDecision | 110 | قرار مخطط تدفق. |
| FlowChartInputOutput | 111 | إدخال وإخراج مخطط تدفق. |
| FlowChartPredefinedProcess | 112 | عملية مسبقة التعريف في مخطط تدفق. |
| FlowChartInternalStorage | 113 | التخزين الداخلي لمخطط التدفق. |
| FlowChartDocument | 114 | مستند مخطط التدفق. |
| FlowChartMultidocument | 115 | مستند متعدد لمخطط التدفق. |
| FlowChartTerminator | 116 | منهي مخطط التدفق. |
| FlowChartPreparation | 117 | تحضير مخطط التدفق. |
| FlowChartManualInput | 118 | إدخال يدوي لمخطط التدفق. |
| FlowChartManualOperation | 119 | عملية يدوية لمخطط التدفق. |
| FlowChartConnector | 120 | موصل مخطط التدفق. |
| FlowChartPunchedCard | 121 | بطاقة مثقوبة لمخطط التدفق. |
| FlowChartPunchedTape | 122 | شريط مثقوب لمخطط التدفق. |
| FlowChartSummingJunction | 123 | تقاطع جمع لمخطط التدفق. |
| FlowChartOr | 124 | أو مخطط التدفق. |
| FlowChartCollate | 125 | دمج مخطط التدفق. |
| FlowChartSort | 126 | فرز مخطط التدفق. |
| FlowChartExtract | 127 | استخراج مخطط التدفق. |
| FlowChartMerge | 128 | دمج مخطط التدفق. |
| FlowChartOfflineStorage | 129 | تخزين مخطط التدفق غير المتصل. |
| FlowChartOnlineStorage | 130 | تخزين مخطط التدفق المتصل. |
| FlowChartMagneticTape | 131 | شريط مغناطيسي لمخطط التدفق. |
| FlowChartMagneticDisk | 132 | قرص مغناطيسي لمخطط التدفق. |
| FlowChartMagneticDrum | 133 | اسطوانة مغناطيسية لمخطط التدفق. |
| FlowChartDisplay | 134 | عرض مخطط التدفق. |
| FlowChartDelay | 135 | تأخير مخطط التدفق. |
| TextPlainText | 136 | نص عادي، كائن WordArt. |
| TextStop | 137 | إيقاف، كائن WordArt. |
| TextTriangle | 138 | مثلث، كائن WordArt. |
| TextTriangleInverted | 139 | مثلث مقلوب، كائن WordArt. |
| TextChevron | 140 | شيفرون، كائن WordArt. |
| TextChevronInverted | 141 | شيفرون مقلوب، كائن WordArt. |
| TextRingInside | 142 | حلقة داخلية، كائن WordArt. |
| TextRingOutside | 143 | حلقة خارجية، كائن WordArt. |
| TextArchUpCurve | 144 | قوس منحنى صاعد، كائن WordArt. |
| TextArchDownCurve | 145 | قوس منحنى هابط، كائن WordArt. |
| TextCircleCurve | 146 | منحنى دائرة، كائن WordArt. |
| TextButtonCurve | 147 | منحنى زر، كائن WordArt. |
| TextArchUpPour | 148 | قوس صب صاعد، كائن WordArt. |
| TextArchDownPour | 149 | قوس صب هابط، كائن WordArt. |
| TextCirclePour | 150 | صبة دائرة، كائن WordArt. |
| TextButtonPour | 151 | زر صب، كائن WordArt. |
| TextCurveUp | 152 | منحنى للأعلى، كائن WordArt. |
| TextCurveDown | 153 | منحنى للأسفل، كائن WordArt. |
| TextCascadeUp | 154 | تسلسل للأعلى، كائن WordArt. |
| TextCascadeDown | 155 | تسلسل للأسفل، كائن WordArt. |
| TextWave1 | 156 | موجة 1، كائن WordArt. |
| TextWave2 | 157 | موجة 2، كائن WordArt. |
| TextWave3 | 158 | موجة 3، كائن WordArt. |
| TextWave4 | 159 | موجة 4، كائن WordArt. |
| TextInflate | 160 | تضخم، كائن WordArt. |
| TextDeflate | 161 | انكماش، كائن WordArt. |
| TextInflateBottom | 162 | تضخم أسفل، كائن WordArt. |
| TextDeflateBottom | 163 | تقليل الأسفل، WordArt object. |
| TextInflateTop | 164 | تكبير الأعلى، WordArt object. |
| TextDeflateTop | 165 | تقليل الأعلى، WordArt object. |
| TextDeflateInflate | 166 | تقليل وتكبير، WordArt object. |
| TextDeflateInflateDeflate | 167 | تقليل وتكبير وتقليل، WordArt object. |
| TextFadeRight | 168 | تلاشي إلى اليمين، WordArt object. |
| TextFadeLeft | 169 | تلاشي إلى اليسار، WordArt object. |
| TextFadeUp | 170 | تلاشي إلى الأعلى، WordArt object. |
| TextFadeDown | 171 | تلاشي إلى الأسفل، WordArt object. |
| TextSlantUp | 172 | انحدار إلى الأعلى، WordArt object. |
| TextSlantDown | 173 | انحدار إلى الأسفل، WordArt object. |
| TextCanUp | 174 | رفع، WordArt object. |
| TextCanDown | 175 | خفض، WordArt object. |
| FlowChartAlternateProcess | 176 | مخطط تدفق عملية بديلة. |
| FlowChartOffpageConnector | 177 | موصل مخطط تدفق خارج الصفحة. |
| Callout90 | 178 | ملاحظة 90. |
| AccentCallout90 | 179 | ملاحظة مميزة 90. |
| BorderCallout90 | 180 | [Border](../../aspose.words/border/) ملاحظة 90. |
| AccentBorderCallout90 | 181 | ملاحظة حدود مميزة 90. |
| LeftRightUpArrow | 182 | سهم يسار يمين أعلى. |
| Sun | 183 | شمس. |
| Moon | 184 | قمر. |
| BracketPair | 185 | زوج أقواس. |
| BracePair | 186 | زوج أقواس معقوفة. |
| Seal4 | 187 | نجم بأربع نقاط. |
| DoubleWave | 188 | موجة مزدوجة. |
| ActionButtonBlank | 189 | زر الإجراء فارغ. |
| ActionButtonHome | 190 | زر الإجراء للصفحة الرئيسية. |
| ActionButtonHelp | 191 | زر الإجراء للمساعدة. |
| ActionButtonInformation | 192 | زر الإجراء للمعلومات. |
| ActionButtonForwardNext | 193 | زر الإجراء للأمام التالي. |
| ActionButtonBackPrevious | 194 | زر الإجراء للعودة السابق. |
| ActionButtonEnd | 195 | زر الإجراء للنهاية. |
| ActionButtonBeginning | 196 | زر الإجراء للبداية. |
| ActionButtonReturn | 197 | زر الإجراء للعودة. |
| ActionButtonDocument | 198 | زر الإجراء للمستند. |
| ActionButtonSound | 199 | زر الإجراء للصوت. |
| ActionButtonMovie | 200 | زر الإجراء للفيلم. |
| SingleCornerSnipped | 203 | قص زاوية واحدة لمستطيل الكائن. |
| TopCornersSnipped | 204 | قص مستطيل الزاوية على نفس الجانب. |
| DiagonalCornersSnipped | 205 | قص مستطيل الزاوية القطرية. |
| TopCornersOneRoundedOneSnipped | 206 | قص وتدوير مستطيل الزاوية الواحدة. |
| SingleCornerRounded | 207 | تدوير مستطيل الزاوية الواحدة. |
| TopCornersRounded | 208 | تدوير مستطيل الزاوية على نفس الجانب. |
| DiagonalCornersRounded | 209 | تدوير مستطيل الزاوية القطرية. |
| Heptagon | 210 | سباعي الأضلاع. |
| Cloud | 211 | سحابة. |
| Seal6 | 212 | نجمة ذات ست نقاط. |
| Seal7 | 213 | نجمة ذات سبع نقاط. |
| Seal10 | 214 | نجمة ذات عشر نقاط. |
| Seal12 | 215 | نجمة ذات اثنتا عشر نقطة. |
| SwooshArrow | 216 | سهم سوش. |
| قطرة دم | 217 | قطرة دم. |
| علامات مربعة | 218 | علامات مربعة. |
| علامات لوحة | 219 | علامات لوحة. |
| فطيرة | 220 | فطيرة. |
| فطيرة قطاع | 221 | فطيرة قطاع. |
| خط عكسي | 222 | خط عكسي. |
| MathPlus | 223 | [Math](../../aspose.words.math/) زائد. |
| MathMinus | 224 | [Math](../../aspose.words.math/) ناقص. |
| MathMultiply | 225 | [Math](../../aspose.words.math/) ضرب. |
| MathDivide | 226 | [Math](../../aspose.words.math/) قسمة. |
| MathEqual | 227 | [Math](../../aspose.words.math/) يساوي. |
| MathNotEqual | 228 | [Math](../../aspose.words.math/) ليس مساوياً. |
| مُقَطِّع غير متساوي الساقين | 229 | مُقَطِّع غير متساوي الساقين. |
| سهم دائري يسار-يمين | 230 | سهم دائري يسار-يمين. |
| شريط يسار-يمين | 231 | شريط يسار-يمين. |
| LeftCircularArrow | 232 | سهم دائري إلى اليسار. |
| إطار | 233 | إطار. |
| HalfFrame | 234 | نصف إطار. |
| قمع | 235 | قمع. |
| Gear6 | 236 | ترس ذو ست أسنان. |
| Gear9 | 237 | ترس ذو تسع أسنان. |
| عشاري | 238 | عشاري. |
| ثنائي عشر | 239 | ثنائي عشر. |
| DiagonalStripe | 240 | شريط مائل. |
| زاوية | 241 | زاوية. |
| CornerTabs | 242 | علامات الزاوية. |
| وتر | 243 | وتر. |
| ChartPlus | 244 | مخطط زائد. |
| ChartStar | 245 | مخطط نجمة. |
| ChartX | 246 | مخطط X. |
| MinValue | n/a | محجوز لاستخدام النظام. |


## أمثلة



يعرض كيفية إدراج شكل مع صورة من نظام الملفات المحلي في مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// المُنشئ العام لفئة "Shape" سيُنشئ شكلاً بنوع الترميز "ShapeMarkupLanguage.Vml".
// إذا كنت بحاجة إلى إنشاء شكل من نوع غير أولي، مثل SingleCornerSnipped، TopCornersSnipped، DiagonalCornersSnipped،
// TopCornersOneRoundedOneSnipped، SingleCornerRounded، TopCornersRounded، أو DiagonalCornersRounded،
// يرجى استخدام DocumentBuilder.InsertShape.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Image);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Windows MetaFile.wmf");
shape->set_Width(100);
shape->set_Height(100);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

doc->Save(get_ArtifactsDir() + u"Image.FromFile.docx");
```


يعرض كيفية تحديد Aspose.Words للأشكال.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertShape(Aspose::Words::Drawing::ShapeType::Heptagon, Aspose::Words::Drawing::RelativeHorizontalPosition::Page, 0, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 0, 0, 0, Aspose::Words::Drawing::WrapType::None);

builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cloud, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, 0, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 0, 0, 0, Aspose::Words::Drawing::WrapType::None);

builder->InsertShape(Aspose::Words::Drawing::ShapeType::MathPlus, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, 0, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 0, 0, 0, Aspose::Words::Drawing::WrapType::None);

// لتحديد أنواع الأشكال بشكل صحيح تحتاج إلى العمل مع الأشكال كـ DML.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
// التوافق "Strict" أو "Transitional" يسمح بحفظ الشكل كـ DML.
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(get_ArtifactsDir() + u"Shape.ShapeTypes.docx", saveOptions);
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.ShapeTypes.docx");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

for (System::SharedPtr<Aspose::Words::Drawing::Shape> shape : shapes)
{
    std::cout << System::EnumGetName(shape->get_ShapeType()) << std::endl;
}
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
