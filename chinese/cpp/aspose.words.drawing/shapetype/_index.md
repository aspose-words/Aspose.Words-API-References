---
title: "Aspose::Words::Drawing::ShapeType 枚举"
linktitle: "ShapeType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeType 枚举。指定在 C++ 中的 Microsoft Word 文档中形状的类型。"
type: docs
weight: 38000
url: /zh/cpp/aspose.words.drawing/shapetype/
---
## ShapeType enum


指定 Microsoft Word 文档中形状的类型。

```cpp
enum class ShapeType
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 图像 | 75 | 该形状是图像。 |
| 文本框 | 202 | 该形状是文本框。请注意，许多其他类型的形状也可以包含文本。形状不一定必须是此类型才能包含文本。 |
| Group | -1 | 该形状是组合形状。 |
| OleObject | -2 | 该形状是 OLE 对象。您不能在文档中创建此类型的形状。 |
| OleControl | 201 | 该形状是 ActiveX 控件。您不能在文档中创建此类型的形状。 |
| NonPrimitive | 0 | 由用户绘制且由多个线段和/或顶点（曲线、自由形或涂鸦）组成的形状。您不能在文档中创建此类型的形状。 |
| Rectangle | 1 | 矩形。 |
| RoundRectangle | 2 | 圆角矩形。 |
| Ellipse | 3 | 椭圆。 |
| 钻石 | 4 | 钻石。 |
| 三角形 | 5 | 三角形。 |
| 直角三角形 | 6 | 直角三角形。 |
| 平行四边形 | 7 | 平行四边形。 |
| 梯形 | 8 | 梯形。 |
| 六边形 | 9 | 六边形。 |
| 八边形 | 10 | 八边形。 |
| 加号 | 11 | 加号。 |
| 星形 | 12 | 星形。 |
| 箭头 | 13 | 箭头。 |
| 粗箭头 | 14 | 粗箭头。 |
| 本垒板 | 15 | 本垒板。 |
| 立方体 | 16 | 立方体。 |
| 气球 | 17 | 气球。 |
| 封印 | 18 | 封印。 |
| 弧线 | 19 | 弧线。 |
| 线 | 20 | 线条。 |
| 匾牌 | 21 | 匾牌。 |
| 罐子 | 22 | 罐子。 |
| 甜甜圈 | 23 | 甜甜圈。 |
| 文本简易 | 24 | 文本 简单。 |
| 文本八边形 | 25 | 文本 八边形。 |
| 文本六边形 | 26 | 文本 六边形。 |
| 文本曲线 | 27 | 文本 曲线。 |
| 文本波形 | 28 | 文本 波形。 |
| 文本环形 | 29 | 文本环。 |
| TextOnCurve | 30 | 文本在曲线上。 |
| TextOnRing | 31 | 文本在环上。 |
| StraightConnector1 | 32 | 一个直线连接器形状。 |
| BentConnector2 | 33 | 一个由两个段组成的弯曲连接器形状。 |
| BentConnector3 | 34 | 一个由三个段组成的弯曲连接器形状。 |
| BentConnector4 | 35 | 一个由四个段组成的弯曲连接器形状。 |
| BentConnector5 | 36 | 一个由五个段组成的弯曲连接器形状。 |
| CurvedConnector2 | 37 | 一个由两个段组成的曲线连接器形状。 |
| CurvedConnector3 | 38 | 一个由三个段组成的曲线连接器形状。 |
| CurvedConnector4 | 39 | 一个由四个段组成的曲线连接器形状。 |
| CurvedConnector5 | 40 | 一个由五个段组成的曲线连接器形状。 |
| Callout1 | 41 | 一个带有一个箭头的标注形状。 |
| Callout2 | 42 | 一个带有两个箭头的标注形状。 |
| Callout3 | 43 | 一个带有三个箭头的标注形状。 |
| AccentCallout1 | 44 | 一个带有一个箭头的强调标注形状。 |
| AccentCallout2 | 45 | 一个带有两个箭头的强调标注形状。 |
| AccentCallout3 | 46 | 一个带有三个箭头的强调标注形状。 |
| BorderCallout1 | 47 | [Border](../../aspose.words/border/) 标注 1。 |
| BorderCallout2 | 48 | [Border](../../aspose.words/border/) 标注 2。 |
| BorderCallout3 | 49 | [Border](../../aspose.words/border/) 标注 3。 |
| AccentBorderCallout1 | 50 | 强调边框标注 1。 |
| AccentBorderCallout2 | 51 | 强调边框标注 2。 |
| AccentBorderCallout3 | 52 | 强调边框标注 3。 |
| Ribbon | 53 | Ribbon。 |
| Ribbon2 | 54 | Ribbon 2。 |
| Chevron | 55 | Chevron。 |
| 五边形 | 56 | 五边形。 |
| 禁止吸烟 | 57 | 禁止吸烟。 |
| Seal8 | 58 | 八角星。 |
| Seal16 | 59 | 十六角星。 |
| Seal32 | 60 | 三十二角星。 |
| WedgeRectCallout | 61 | 楔形矩形标注。 |
| WedgeRRectCallout | 62 | 楔形圆角矩形标注。 |
| WedgeEllipseCallout | 63 | 楔形椭圆标注。 |
| Wave | 64 | 波形。 |
| FoldedCorner | 65 | 折叠角。 |
| LeftArrow | 66 | 左箭头。 |
| DownArrow | 67 | 下箭头。 |
| UpArrow | 68 | 上箭头。 |
| LeftRightArrow | 69 | 左右箭头。 |
| UpDownArrow | 70 | 上下箭头。 |
| IrregularSeal1 | 71 | 不规则封印 1。 |
| IrregularSeal2 | 72 | 不规则封印 2。 |
| LightningBolt | 73 | 闪电。 |
| Heart | 74 | 心形。 |
| QuadArrow | 76 | 四向箭头。 |
| LeftArrowCallout | 77 | 左箭头标注。 |
| RightArrowCallout | 78 | 右箭头标注。 |
| UpArrowCallout | 79 | 上箭头标注。 |
| DownArrowCallout | 80 | 下箭头标注。 |
| LeftRightArrowCallout | 81 | 左右箭头标注。 |
| UpDownArrowCallout | 82 | 上下箭头标注。 |
| QuadArrowCallout | 83 | 四向箭头标注。 |
| 斜角 | 84 | 斜角。 |
| 左括号 | 85 | 左括号。 |
| 右括号 | 86 | 右括号。 |
| 左大括号 | 87 | 左大括号。 |
| 右大括号 | 88 | 右大括号。 |
| 左上箭头 | 89 | 左上箭头。 |
| 弯曲向上箭头 | 90 | 弯曲向上箭头。 |
| 弯曲箭头 | 91 | 弯曲箭头。 |
| Seal24 | 92 | 24角星。 |
| 条纹右箭头 | 93 | 条纹右箭头。 |
| 缺口右箭头 | 94 | 缺口右箭头。 |
| BlockArc | 95 | 块弧。 |
| SmileyFace | 96 | 笑脸。 |
| VerticalScroll | 97 | 垂直滚动。 |
| HorizontalScroll | 98 | 水平滚动。 |
| CircularArrow | 99 | 圆形箭头。 |
| CustomShape | 100 | 此形状类型似乎用于不属于 Microsoft Word 中自动形状标准集合的形状。例如，如果您从 ClipArt 插入一个新的自动形状。您无法在文档中创建此类型的形状。 |
| UturnArrow | 101 | 掉头箭头。 |
| CurvedRightArrow | 102 | 弯曲右箭头。 |
| CurvedLeftArrow | 103 | 弯曲左箭头。 |
| CurvedUpArrow | 104 | 弯曲上箭头。 |
| CurvedDownArrow | 105 | 弯曲下箭头。 |
| CloudCallout | 106 | 云形标注。 |
| EllipseRibbon | 107 | 椭圆形丝带。 |
| EllipseRibbon2 | 108 | 椭圆形丝带 2。 |
| FlowChartProcess | 109 | 流程图过程。 |
| FlowChartDecision | 110 | 流程图决策。 |
| FlowChartInputOutput | 111 | 流程图输入输出。 |
| FlowChartPredefinedProcess | 112 | 流程图预定义过程。 |
| FlowChartInternalStorage | 113 | 流程图内部存储。 |
| FlowChartDocument | 114 | 流程图文档。 |
| FlowChartMultidocument | 115 | 流程图多文档。 |
| FlowChartTerminator | 116 | 流程图终止符。 |
| FlowChartPreparation | 117 | 流程图准备。 |
| FlowChartManualInput | 118 | 流程图手动输入。 |
| FlowChartManualOperation | 119 | 流程图手动操作。 |
| FlowChartConnector | 120 | 流程图连接器。 |
| FlowChartPunchedCard | 121 | 流程图穿孔卡。 |
| FlowChartPunchedTape | 122 | 流程图穿孔磁带。 |
| FlowChartSummingJunction | 123 | 流程图求和节点。 |
| FlowChartOr | 124 | 流程图或。 |
| FlowChartCollate | 125 | 流程图合并。 |
| FlowChartSort | 126 | 流程图排序。 |
| FlowChartExtract | 127 | 流程图提取。 |
| FlowChartMerge | 128 | 流程图合并。 |
| FlowChartOfflineStorage | 129 | 流程图离线存储。 |
| FlowChartOnlineStorage | 130 | 流程图在线存储。 |
| FlowChartMagneticTape | 131 | 流程字符磁带。 |
| FlowChartMagneticDisk | 132 | 流程图磁盘。 |
| FlowChartMagneticDrum | 133 | 流程图磁鼓。 |
| FlowChartDisplay | 134 | 流程图显示。 |
| FlowChartDelay | 135 | 流程图延迟。 |
| TextPlainText | 136 | 纯文本，WordArt 对象。 |
| TextStop | 137 | 停止，WordArt 对象。 |
| TextTriangle | 138 | 三角形，WordArt 对象。 |
| TextTriangleInverted | 139 | 倒置三角形，WordArt 对象。 |
| TextChevron | 140 | V形，WordArt 对象。 |
| TextChevronInverted | 141 | 倒置 V 形，WordArt 对象。 |
| TextRingInside | 142 | 内部环，WordArt 对象。 |
| TextRingOutside | 143 | 外部环，WordArt 对象。 |
| TextArchUpCurve | 144 | 拱形上曲线，WordArt 对象。 |
| TextArchDownCurve | 145 | 拱形下曲线，WordArt 对象。 |
| TextCircleCurve | 146 | 圆形曲线，WordArt 对象。 |
| TextButtonCurve | 147 | 按钮曲线，WordArt 对象。 |
| TextArchUpPour | 148 | 拱形上倾，WordArt 对象。 |
| TextArchDownPour | 149 | 拱形下倾，WordArt 对象。 |
| TextCirclePour | 150 | 圆形倾，WordArt 对象。 |
| TextButtonPour | 151 | 按钮倾，WordArt 对象。 |
| TextCurveUp | 152 | 曲线向上，WordArt 对象。 |
| TextCurveDown | 153 | 曲线向下，WordArt 对象。 |
| TextCascadeUp | 154 | 层叠向上，WordArt 对象。 |
| TextCascadeDown | 155 | 层叠向下，WordArt 对象。 |
| TextWave1 | 156 | 波形 1，WordArt 对象。 |
| TextWave2 | 157 | 波形 2，WordArt 对象。 |
| TextWave3 | 158 | 波形 3，WordArt 对象。 |
| TextWave4 | 159 | 波形 4，WordArt 对象。 |
| TextInflate | 160 | 膨胀，WordArt 对象。 |
| TextDeflate | 161 | 收缩，WordArt 对象。 |
| TextInflateBottom | 162 | 底部膨胀，WordArt 对象。 |
| TextDeflateBottom | 163 | 底部收缩，WordArt 对象。 |
| TextInflateTop | 164 | 顶部膨胀，WordArt 对象。 |
| TextDeflateTop | 165 | 顶部收缩，WordArt 对象。 |
| TextDeflateInflate | 166 | 收缩膨胀，WordArt 对象。 |
| TextDeflateInflateDeflate | 167 | 收缩膨胀收缩，WordArt 对象。 |
| TextFadeRight | 168 | 向右淡出，WordArt 对象。 |
| TextFadeLeft | 169 | 向左淡出，WordArt 对象。 |
| TextFadeUp | 170 | 向上淡出，WordArt 对象。 |
| TextFadeDown | 171 | 向下淡出，WordArt 对象。 |
| TextSlantUp | 172 | 向上倾斜，WordArt 对象。 |
| TextSlantDown | 173 | 向下倾斜，WordArt 对象。 |
| TextCanUp | 174 | 向上倾斜，WordArt 对象。 |
| TextCanDown | 175 | 向下倾斜，WordArt 对象。 |
| FlowChartAlternateProcess | 176 | 流程图交替过程。 |
| FlowChartOffpageConnector | 177 | 流程图跨页连接器。 |
| Callout90 | 178 | 标注 90。 |
| AccentCallout90 | 179 | 强调标注 90。 |
| BorderCallout90 | 180 | [Border](../../aspose.words/border/) 标注 90。 |
| AccentBorderCallout90 | 181 | 强调边框标注 90。 |
| LeftRightUpArrow | 182 | 左 右 上 箭头。 |
| 太阳 | 183 | 太阳。 |
| 月亮 | 184 | 月亮。 |
| BracketPair | 185 | 括号对。 |
| BracePair | 186 | 大括号对。 |
| Seal4 | 187 | 四角星。 |
| DoubleWave | 188 | 双波。 |
| ActionButtonBlank | 189 | 操作按钮空白。 |
| ActionButtonHome | 190 | 操作按钮主页。 |
| ActionButtonHelp | 191 | 操作按钮帮助。 |
| ActionButtonInformation | 192 | 操作按钮信息。 |
| ActionButtonForwardNext | 193 | 操作按钮前进下一步。 |
| ActionButtonBackPrevious | 194 | 操作按钮后退上一步。 |
| ActionButtonEnd | 195 | 操作按钮结束。 |
| ActionButtonBeginning | 196 | 操作按钮开始。 |
| ActionButtonReturn | 197 | 操作按钮返回。 |
| ActionButtonDocument | 198 | 操作按钮文档。 |
| ActionButtonSound | 199 | 操作按钮声音。 |
| ActionButtonMovie | 200 | 操作按钮视频。 |
| SingleCornerSnipped | 203 | 剪切单角矩形对象。 |
| TopCornersSnipped | 204 | 剪切同侧角矩形。 |
| DiagonalCornersSnipped | 205 | 剪切对角角矩形。 |
| TopCornersOneRoundedOneSnipped | 206 | 剪切并圆化单角矩形。 |
| SingleCornerRounded | 207 | 圆化单角矩形。 |
| TopCornersRounded | 208 | 圆化同侧角矩形。 |
| DiagonalCornersRounded | 209 | 圆化对角角矩形。 |
| 七边形 | 210 | 七边形。 |
| 云 | 211 | 云。 |
| Seal6 | 212 | 六角星。 |
| Seal7 | 213 | 七角星。 |
| Seal10 | 214 | 十角星。 |
| Seal12 | 215 | 十二角星。 |
| SwooshArrow | 216 | 弧形箭头。 |
| 泪滴形 | 217 | 泪滴形。 |
| SquareTabs | 218 | 方形标签。 |
| PlaqueTabs | 219 | 牌匾标签。 |
| 饼图 | 220 | 饼图。 |
| WedgePie | 221 | 楔形饼图。 |
| InverseLine | 222 | 反向线。 |
| MathPlus | 223 | [Math](../../aspose.words.math/) 加。 |
| MathMinus | 224 | [Math](../../aspose.words.math/) 减。 |
| MathMultiply | 225 | [Math](../../aspose.words.math/) 乘。 |
| MathDivide | 226 | [Math](../../aspose.words.math/) 除。 |
| MathEqual | 227 | [Math](../../aspose.words.math/) 等于。 |
| MathNotEqual | 228 | [Math](../../aspose.words.math/) 不等于。 |
| 非等腰梯形 | 229 | 非等腰梯形。 |
| 左右循环箭头 | 230 | 左右循环箭头。 |
| 左右丝带 | 231 | 左右丝带。 |
| 左循环箭头 | 232 | 左循环箭头。 |
| 框架 | 233 | 框架。 |
| 半框架 | 234 | 半框架。 |
| 漏斗 | 235 | 漏斗。 |
| 六齿齿轮 | 236 | 六齿齿轮。 |
| 九齿齿轮 | 237 | 九齿齿轮。 |
| 十边形 | 238 | 十边形。 |
| 十二边形 | 239 | 十二边形。 |
| 对角线条纹 | 240 | 对角线条纹。 |
| 拐角 | 241 | 拐角。 |
| 拐角标签 | 242 | 拐角标签。 |
| 弦线 | 243 | 弦线。 |
| 图表加 | 244 | 图表加。 |
| 图表星形 | 245 | 图表星形。 |
| 图表X | 246 | 图表 X。 |
| 最小值 | n/a | 保留供系统使用。 |


## 示例



展示如何将本地文件系统中的图像插入为形状到文档中。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// "Shape" 类的公共构造函数将创建一个使用 "ShapeMarkupLanguage.Vml" 标记类型的形状。
// 如果需要创建非原始类型的形状，例如 SingleCornerSnipped、TopCornersSnipped、DiagonalCornersSnipped，
// TopCornersOneRoundedOneSnipped、SingleCornerRounded、TopCornersRounded 或 DiagonalCornersRounded，
// 请使用 DocumentBuilder.InsertShape。
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Image);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Windows MetaFile.wmf");
shape->set_Width(100);
shape->set_Height(100);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

doc->Save(get_ArtifactsDir() + u"Image.FromFile.docx");
```


展示 Aspose.Words 如何识别形状。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertShape(Aspose::Words::Drawing::ShapeType::Heptagon, Aspose::Words::Drawing::RelativeHorizontalPosition::Page, 0, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 0, 0, 0, Aspose::Words::Drawing::WrapType::None);

builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cloud, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, 0, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 0, 0, 0, Aspose::Words::Drawing::WrapType::None);

builder->InsertShape(Aspose::Words::Drawing::ShapeType::MathPlus, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, 0, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 0, 0, 0, Aspose::Words::Drawing::WrapType::None);

// 要正确识别形状类型，您需要将形状视为 DML 来处理。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
// \"Strict\" 或 \"Transitional\" 合规性允许将形状保存为 DML。
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(get_ArtifactsDir() + u"Shape.ShapeTypes.docx", saveOptions);
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.ShapeTypes.docx");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

for (System::SharedPtr<Aspose::Words::Drawing::Shape> shape : shapes)
{
    std::cout << System::EnumGetName(shape->get_ShapeType()) << std::endl;
}
```

## 另见

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
