---
title: "ChartShapeType"
linktitle: "ChartShapeType"
second_title: "Aspose.Words for Java"
description: "指定 Java 中图表元素的形状类型。"
type: docs
weight: 90
url: /zh/java/com.aspose.words/chartshapetype/
---

**Inheritance:**
java.lang.Object
```
public class ChartShapeType
```

指定图表元素的形状类型。

 **Examples:** 

展示如何为图表数据标签设置填充、描边和标注格式。

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete default generated series.
 chart.getSeries().clear();

 // Add new series.
 ChartSeries series = chart.getSeries().add("AW Series 1",
         new String[] { "AW Category 1", "AW Category 2", "AW Category 3", "AW Category 4" },
         new double[] { 100.0, 200.0, 300.0, 400.0 });

 // Show data labels.
 series.hasDataLabels(true);
 series.getDataLabels().setShowValue(true);

 // Format data labels as callouts.
 ChartFormat format = series.getDataLabels().getFormat();
 format.setShapeType(ChartShapeType.WEDGE_RECT_CALLOUT);
 format.getStroke().setColor(Color.lightGray);
 format.getFill().solid(Color.GREEN);
 series.getDataLabels().getFont().setColor(Color.YELLOW);

 // Change fill and stroke of an individual data label.
 ChartFormat labelFormat = series.getDataLabels().get(0).getFormat();
 labelFormat.getStroke().setColor(Color.BLUE);
 labelFormat.getFill().solid(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.FormatDataLables.docx");
 
```
## 字段集合

| 字段 | 描述 |
| --- | --- |
| [ACCENT_BORDER_CALLOUT_1](#ACCENT-BORDER-CALLOUT-1) | 带边框 1 的强调标注。 |
| [ACCENT_BORDER_CALLOUT_2](#ACCENT-BORDER-CALLOUT-2) | 带边框 2 的强调标注。 |
| [ACCENT_BORDER_CALLOUT_3](#ACCENT-BORDER-CALLOUT-3) | 带边框 3 的强调标注。 |
| [ACCENT_CALLOUT_1](#ACCENT-CALLOUT-1) | 强调标注 1。 |
| [ACCENT_CALLOUT_2](#ACCENT-CALLOUT-2) | 强调标注 2。 |
| [ACCENT_CALLOUT_3](#ACCENT-CALLOUT-3) | 强调标注 3。 |
| [ACTION_BUTTON_BACK_PREVIOUS](#ACTION-BUTTON-BACK-PREVIOUS) | 后退或上一步按钮。 |
| [ACTION_BUTTON_BEGINNING](#ACTION-BUTTON-BEGINNING) | 开始按钮。 |
| [ACTION_BUTTON_BLANK](#ACTION-BUTTON-BLANK) | 空白按钮。 |
| [ACTION_BUTTON_DOCUMENT](#ACTION-BUTTON-DOCUMENT) | 文档按钮。 |
| [ACTION_BUTTON_END](#ACTION-BUTTON-END) | 结束按钮。 |
| [ACTION_BUTTON_FORWARD_NEXT](#ACTION-BUTTON-FORWARD-NEXT) | 前进或下一步按钮。 |
| [ACTION_BUTTON_HELP](#ACTION-BUTTON-HELP) | 帮助按钮。 |
| [ACTION_BUTTON_HOME](#ACTION-BUTTON-HOME) | 主页按钮。 |
| [ACTION_BUTTON_INFORMATION](#ACTION-BUTTON-INFORMATION) | 信息按钮。 |
| [ACTION_BUTTON_MOVIE](#ACTION-BUTTON-MOVIE) | 电影按钮。 |
| [ACTION_BUTTON_RETURN](#ACTION-BUTTON-RETURN) | 返回按钮。 |
| [ACTION_BUTTON_SOUND](#ACTION-BUTTON-SOUND) | 声音按钮. |
| [ARC](#ARC) | 弧形. |
| [ARROW](#ARROW) | 箭头. |
| [BENT_ARROW](#BENT-ARROW) | 弯曲箭头. |
| [BENT_CONNECTOR_2](#BENT-CONNECTOR-2) | 弯曲连接器 2. |
| [BENT_CONNECTOR_3](#BENT-CONNECTOR-3) | 弯曲连接器 3. |
| [BENT_CONNECTOR_4](#BENT-CONNECTOR-4) | 弯曲连接器 4. |
| [BENT_CONNECTOR_5](#BENT-CONNECTOR-5) | 弯曲连接器 5. |
| [BENT_UP_ARROW](#BENT-UP-ARROW) | 向上弯曲箭头. |
| [BEVEL](#BEVEL) | 斜角. |
| [BLOCK_ARC](#BLOCK-ARC) | 块状弧形. |
| [BORDER_CALLOUT_1](#BORDER-CALLOUT-1) | 带边框的标注 1. |
| [BORDER_CALLOUT_2](#BORDER-CALLOUT-2) | 带边框的标注 2. |
| [BORDER_CALLOUT_3](#BORDER-CALLOUT-3) | 带边框的标注 3. |
| [BRACE_PAIR](#BRACE-PAIR) | 大括号对. |
| [BRACKET_PAIR](#BRACKET-PAIR) | 方括号对. |
| [CALLOUT_1](#CALLOUT-1) | 标注 1. |
| [CALLOUT_2](#CALLOUT-2) | 标注 2. |
| [CALLOUT_3](#CALLOUT-3) | 标注 3. |
| [CAN](#CAN) | 罐子. |
| [CHART_PLUS](#CHART-PLUS) | 图表加号. |
| [CHART_STAR](#CHART-STAR) | 图表星形. |
| [CHART_X](#CHART-X) | 图表 X. |
| [CHEVRON](#CHEVRON) | 人字形. |
| [CHORD](#CHORD) | 弦. |
| [CIRCULAR_ARROW](#CIRCULAR-ARROW) | 圆形箭头。 |
| [CLOUD](#CLOUD) | 云形。 |
| [CLOUD_CALLOUT](#CLOUD-CALLOUT) | 云形标注。 |
| [CORNER](#CORNER) | 角形。 |
| [CORNER_TABS](#CORNER-TABS) | 角形标签。 |
| [CUBE](#CUBE) | 立方体。 |
| [CURVED_CONNECTOR_2](#CURVED-CONNECTOR-2) | 弯曲连接线 2。 |
| [CURVED_CONNECTOR_3](#CURVED-CONNECTOR-3) | 弯曲连接线 3。 |
| [CURVED_CONNECTOR_4](#CURVED-CONNECTOR-4) | 弯曲连接线 4。 |
| [CURVED_CONNECTOR_5](#CURVED-CONNECTOR-5) | 弯曲连接线 5。 |
| [CURVED_DOWN_ARROW](#CURVED-DOWN-ARROW) | 向下弯曲箭头。 |
| [CURVED_LEFT_ARROW](#CURVED-LEFT-ARROW) | 向左弯曲箭头。 |
| [CURVED_RIGHT_ARROW](#CURVED-RIGHT-ARROW) | 向右弯曲箭头。 |
| [CURVED_UP_ARROW](#CURVED-UP-ARROW) | 向上弯曲箭头。 |
| [DECAGON](#DECAGON) | 十边形。 |
| [DEFAULT](#DEFAULT) | 指示图表元素未定义形状。 |
| [DIAGONAL_CORNERS_ROUNDED](#DIAGONAL-CORNERS-ROUNDED) | 圆角对角矩形。 |
| [DIAGONAL_CORNERS_SNIPPED](#DIAGONAL-CORNERS-SNIPPED) | 斜切对角矩形。 |
| [DIAGONAL_STRIPE](#DIAGONAL-STRIPE) | 对角条纹。 |
| [DIAMOND](#DIAMOND) | 菱形。 |
| [DODECAGON](#DODECAGON) | 十二边形。 |
| [DONUT](#DONUT) | 环形。 |
| [DOUBLE_WAVE](#DOUBLE-WAVE) | 双波形。 |
| [DOWN_ARROW](#DOWN-ARROW) | 向下箭头。 |
| [DOWN_ARROW_CALLOUT](#DOWN-ARROW-CALLOUT) | 向下标注箭头。 |
| [ELLIPSE](#ELLIPSE) | 椭圆. |
| [ELLIPSE_RIBBON](#ELLIPSE-RIBBON) | 椭圆带. |
| [ELLIPSE_RIBBON_2](#ELLIPSE-RIBBON-2) | 椭圆带 2. |
| [FLOW_CHART_ALTERNATE_PROCESS](#FLOW-CHART-ALTERNATE-PROCESS) | 交替流程. |
| [FLOW_CHART_COLLATE](#FLOW-CHART-COLLATE) | 汇总流程. |
| [FLOW_CHART_CONNECTOR](#FLOW-CHART-CONNECTOR) | 连接器流程. |
| [FLOW_CHART_DECISION](#FLOW-CHART-DECISION) | 决策流程. |
| [FLOW_CHART_DELAY](#FLOW-CHART-DELAY) | 延迟流程. |
| [FLOW_CHART_DISPLAY](#FLOW-CHART-DISPLAY) | 显示流程. |
| [FLOW_CHART_DOCUMENT](#FLOW-CHART-DOCUMENT) | 文档流程. |
| [FLOW_CHART_EXTRACT](#FLOW-CHART-EXTRACT) | 提取流程. |
| [FLOW_CHART_INPUT_OUTPUT](#FLOW-CHART-INPUT-OUTPUT) | 输入输出流程. |
| [FLOW_CHART_INTERNAL_STORAGE](#FLOW-CHART-INTERNAL-STORAGE) | 内部存储流程. |
| [FLOW_CHART_MAGNETIC_DISK](#FLOW-CHART-MAGNETIC-DISK) | 磁盘流程. |
| [FLOW_CHART_MAGNETIC_DRUM](#FLOW-CHART-MAGNETIC-DRUM) | 磁鼓流程. |
| [FLOW_CHART_MAGNETIC_TAPE](#FLOW-CHART-MAGNETIC-TAPE) | 磁带流程. |
| [FLOW_CHART_MANUAL_INPUT](#FLOW-CHART-MANUAL-INPUT) | 手动输入流程. |
| [FLOW_CHART_MANUAL_OPERATION](#FLOW-CHART-MANUAL-OPERATION) | 手动操作流程. |
| [FLOW_CHART_MERGE](#FLOW-CHART-MERGE) | 合并流程. |
| [FLOW_CHART_MULTIDOCUMENT](#FLOW-CHART-MULTIDOCUMENT) | 多文档流程. |
| [FLOW_CHART_OFFLINE_STORAGE](#FLOW-CHART-OFFLINE-STORAGE) | 离线存储流程. |
| [FLOW_CHART_OFFPAGE_CONNECTOR](#FLOW-CHART-OFFPAGE-CONNECTOR) | 页外连接器流程. |
| [FLOW_CHART_ONLINE_STORAGE](#FLOW-CHART-ONLINE-STORAGE) | 在线存储流程. |
| [FLOW_CHART_OR](#FLOW-CHART-OR) | 或流程. |
| [FLOW_CHART_PREDEFINED_PROCESS](#FLOW-CHART-PREDEFINED-PROCESS) | 预定义流程. |
| [FLOW_CHART_PREPARATION](#FLOW-CHART-PREPARATION) | 准备流程。 |
| [FLOW_CHART_PROCESS](#FLOW-CHART-PROCESS) | 处理流程。 |
| [FLOW_CHART_PUNCHED_CARD](#FLOW-CHART-PUNCHED-CARD) | 穿孔卡片流程。 |
| [FLOW_CHART_PUNCHED_TAPE](#FLOW-CHART-PUNCHED-TAPE) | 穿孔纸带流程。 |
| [FLOW_CHART_SORT](#FLOW-CHART-SORT) | 排序流程。 |
| [FLOW_CHART_SUMMING_JUNCTION](#FLOW-CHART-SUMMING-JUNCTION) | 求和节点流程。 |
| [FLOW_CHART_TERMINATOR](#FLOW-CHART-TERMINATOR) | 终止符流程。 |
| [FOLDED_CORNER](#FOLDED-CORNER) | 折叠角。 |
| [FRAME](#FRAME) | 框架。 |
| [FUNNEL](#FUNNEL) | 漏斗。 |
| [GEAR_6](#GEAR-6) | 六齿齿轮。 |
| [GEAR_9](#GEAR-9) | 九齿齿轮。 |
| [HALF_FRAME](#HALF-FRAME) | 半框架。 |
| [HEART](#HEART) | 心形。 |
| [HEPTAGON](#HEPTAGON) | 七边形。 |
| [HEXAGON](#HEXAGON) | 六边形。 |
| [HOME_PLATE](#HOME-PLATE) | 本垒。 |
| [HORIZONTAL_SCROLL](#HORIZONTAL-SCROLL) | 水平滚动。 |
| [INVERSE_LINE](#INVERSE-LINE) | 反向线。 |
| [IRREGULAR_SEAL_1](#IRREGULAR-SEAL-1) | 不规则密封 1。 |
| [IRREGULAR_SEAL_2](#IRREGULAR-SEAL-2) | 不规则密封 2。 |
| [LEFT_ARROW](#LEFT-ARROW) | 左箭头。 |
| [LEFT_ARROW_CALLOUT](#LEFT-ARROW-CALLOUT) | 标注左箭头。 |
| [LEFT_BRACE](#LEFT-BRACE) | 左大括号。 |
| [LEFT_BRACKET](#LEFT-BRACKET) | 左方括号。 |
| [LEFT_CIRCULAR_ARROW](#LEFT-CIRCULAR-ARROW) | 左循环箭头。 |
| [LEFT_RIGHT_ARROW](#LEFT-RIGHT-ARROW) | 左和右箭头。 |
| [LEFT_RIGHT_ARROW_CALLOUT](#LEFT-RIGHT-ARROW-CALLOUT) | 标注左和右箭头。 |
| [LEFT_RIGHT_CIRCULAR_ARROW](#LEFT-RIGHT-CIRCULAR-ARROW) | 左右循环箭头。 |
| [LEFT_RIGHT_RIBBON](#LEFT-RIGHT-RIBBON) | 左右丝带。 |
| [LEFT_RIGHT_UP_ARROW](#LEFT-RIGHT-UP-ARROW) | 左右向上箭头。 |
| [LEFT_UP_ARROW](#LEFT-UP-ARROW) | 左上箭头。 |
| [LIGHTNING_BOLT](#LIGHTNING-BOLT) | 闪电。 |
| [LINE](#LINE) | 线条。 |
| [MATH_DIVIDE](#MATH-DIVIDE) | 数学除号。 |
| [MATH_EQUAL](#MATH-EQUAL) | 数学等号。 |
| [MATH_MINUS](#MATH-MINUS) | 数学减号。 |
| [MATH_MULTIPLY](#MATH-MULTIPLY) | 数学乘号。 |
| [MATH_NOT_EQUAL](#MATH-NOT-EQUAL) | 数学不等号。 |
| [MATH_PLUS](#MATH-PLUS) | 数学加号。 |
| [MOON](#MOON) | 月亮。 |
| [NON_ISOSCELES_TRAPEZOID](#NON-ISOSCELES-TRAPEZOID) | 非等腰梯形。 |
| [NOTCHED_RIGHT_ARROW](#NOTCHED-RIGHT-ARROW) | 缺口右箭头。 |
| [NO_SMOKING](#NO-SMOKING) | 禁止吸烟。 |
| [OCTAGON](#OCTAGON) | 八边形。 |
| [PARALLELOGRAM](#PARALLELOGRAM) | 平行四边形。 |
| [PENTAGON](#PENTAGON) | 五边形。 |
| [PIE](#PIE) | 饼图。 |
| [PLAQUE](#PLAQUE) | 牌匾。 |
| [PLAQUE_TABS](#PLAQUE-TABS) | 牌匾标签。 |
| [PLUS](#PLUS) | 加号。 |
| [QUAD_ARROW](#QUAD-ARROW) | 四向箭头。 |
| [QUAD_ARROW_CALLOUT](#QUAD-ARROW-CALLOUT) | 注释四向箭头。 |
| [RECTANGLE](#RECTANGLE) | 矩形。 |
| [RIBBON](#RIBBON) | 丝带。 |
| [RIBBON_2](#RIBBON-2) | 丝带 2。 |
| [RIGHT_ARROW_CALLOUT](#RIGHT-ARROW-CALLOUT) | 注释右箭头。 |
| [RIGHT_BRACE](#RIGHT-BRACE) | 右大括号。 |
| [RIGHT_BRACKET](#RIGHT-BRACKET) | 右方括号。 |
| [RIGHT_TRIANGLE](#RIGHT-TRIANGLE) | 直角三角形。 |
| [ROUND_RECTANGLE](#ROUND-RECTANGLE) | 圆角矩形。 |
| [SEAL_10](#SEAL-10) | 十角星。 |
| [SEAL_12](#SEAL-12) | 十二角星。 |
| [SEAL_16](#SEAL-16) | 十六角星。 |
| [SEAL_24](#SEAL-24) | 二十四角星。 |
| [SEAL_32](#SEAL-32) | 三十二角星。 |
| [SEAL_4](#SEAL-4) | 四角星。 |
| [SEAL_6](#SEAL-6) | 六角星。 |
| [SEAL_7](#SEAL-7) | 七角星。 |
| [SEAL_8](#SEAL-8) | 八角星。 |
| [SINGLE_CORNER_ROUNDED](#SINGLE-CORNER-ROUNDED) | 单角圆角矩形。 |
| [SINGLE_CORNER_SNIPPED](#SINGLE-CORNER-SNIPPED) | 剪切单角矩形对象。 |
| [SMILEY_FACE](#SMILEY-FACE) | 笑脸。 |
| [SQUARE_TABS](#SQUARE-TABS) | 方形标签。 |
| [STAR](#STAR) | 星形。 |
| [STRAIGHT_CONNECTOR_1](#STRAIGHT-CONNECTOR-1) | 直线连接器 1。 |
| [STRIPED_RIGHT_ARROW](#STRIPED-RIGHT-ARROW) | 条纹右箭头。 |
| [SUN](#SUN) | 太阳。 |
| [SWOOSH_ARROW](#SWOOSH-ARROW) | 弧形箭头。 |
| [TEARDROP](#TEARDROP) | 泪滴形。 |
| [TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED](#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED) | 剪切并圆角单角矩形。 |
| [TOP_CORNERS_ROUNDED](#TOP-CORNERS-ROUNDED) | 同侧圆角矩形。 |
| [TOP_CORNERS_SNIPPED](#TOP-CORNERS-SNIPPED) | 同侧剪切角矩形。 |
| [TRAPEZOID](#TRAPEZOID) | 梯形。 |
| [TRIANGLE](#TRIANGLE) | 三角形。 |
| [UP_ARROW](#UP-ARROW) | 向上箭头。 |
| [UP_ARROW_CALLOUT](#UP-ARROW-CALLOUT) | 标注向上箭头。 |
| [UP_DOWN_ARROW](#UP-DOWN-ARROW) | 上下箭头。 |
| [UP_DOWN_ARROW_CALLOUT](#UP-DOWN-ARROW-CALLOUT) | 标注上下箭头。 |
| [UTURN_ARROW](#UTURN-ARROW) | U形转弯箭头。 |
| [VERTICAL_SCROLL](#VERTICAL-SCROLL) | 垂直滚动。 |
| [WAVE](#WAVE) | 波形。 |
| [WEDGE_ELLIPSE_CALLOUT](#WEDGE-ELLIPSE-CALLOUT) | 标注楔形椭圆。 |
| [WEDGE_PIE](#WEDGE-PIE) | 楔形饼图。 |
| [WEDGE_RECT_CALLOUT](#WEDGE-RECT-CALLOUT) | 标注楔形矩形。 |
| [WEDGE_R_RECT_CALLOUT](#WEDGE-R-RECT-CALLOUT) | 标注楔形圆角矩形。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [fromName(String chartShapeTypeName)](#fromName-java.lang.String) |  |
| [getName(int chartShapeType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartShapeType)](#toString-int) |  |
### ACCENT_BORDER_CALLOUT_1 {#ACCENT-BORDER-CALLOUT-1}
```
public static int ACCENT_BORDER_CALLOUT_1
```


带边框 1 的强调标注。

### ACCENT_BORDER_CALLOUT_2 {#ACCENT-BORDER-CALLOUT-2}
```
public static int ACCENT_BORDER_CALLOUT_2
```


带边框 2 的强调标注。

### ACCENT_BORDER_CALLOUT_3 {#ACCENT-BORDER-CALLOUT-3}
```
public static int ACCENT_BORDER_CALLOUT_3
```


带边框 3 的强调标注。

### ACCENT_CALLOUT_1 {#ACCENT-CALLOUT-1}
```
public static int ACCENT_CALLOUT_1
```


强调标注 1。

### ACCENT_CALLOUT_2 {#ACCENT-CALLOUT-2}
```
public static int ACCENT_CALLOUT_2
```


强调标注 2。

### ACCENT_CALLOUT_3 {#ACCENT-CALLOUT-3}
```
public static int ACCENT_CALLOUT_3
```


强调标注 3。

### ACTION_BUTTON_BACK_PREVIOUS {#ACTION-BUTTON-BACK-PREVIOUS}
```
public static int ACTION_BUTTON_BACK_PREVIOUS
```


后退或上一步按钮。

### ACTION_BUTTON_BEGINNING {#ACTION-BUTTON-BEGINNING}
```
public static int ACTION_BUTTON_BEGINNING
```


开始按钮。

### ACTION_BUTTON_BLANK {#ACTION-BUTTON-BLANK}
```
public static int ACTION_BUTTON_BLANK
```


空白按钮。

### ACTION_BUTTON_DOCUMENT {#ACTION-BUTTON-DOCUMENT}
```
public static int ACTION_BUTTON_DOCUMENT
```


文档按钮。

### ACTION_BUTTON_END {#ACTION-BUTTON-END}
```
public static int ACTION_BUTTON_END
```


结束按钮。

### ACTION_BUTTON_FORWARD_NEXT {#ACTION-BUTTON-FORWARD-NEXT}
```
public static int ACTION_BUTTON_FORWARD_NEXT
```


前进或下一步按钮。

### ACTION_BUTTON_HELP {#ACTION-BUTTON-HELP}
```
public static int ACTION_BUTTON_HELP
```


帮助按钮。

### ACTION_BUTTON_HOME {#ACTION-BUTTON-HOME}
```
public static int ACTION_BUTTON_HOME
```


主页按钮。

### ACTION_BUTTON_INFORMATION {#ACTION-BUTTON-INFORMATION}
```
public static int ACTION_BUTTON_INFORMATION
```


信息按钮。

### ACTION_BUTTON_MOVIE {#ACTION-BUTTON-MOVIE}
```
public static int ACTION_BUTTON_MOVIE
```


电影按钮。

### ACTION_BUTTON_RETURN {#ACTION-BUTTON-RETURN}
```
public static int ACTION_BUTTON_RETURN
```


返回按钮。

### ACTION_BUTTON_SOUND {#ACTION-BUTTON-SOUND}
```
public static int ACTION_BUTTON_SOUND
```


声音按钮.

### ARC {#ARC}
```
public static int ARC
```


弧形.

### ARROW {#ARROW}
```
public static int ARROW
```


箭头.

### BENT_ARROW {#BENT-ARROW}
```
public static int BENT_ARROW
```


弯曲箭头.

### BENT_CONNECTOR_2 {#BENT-CONNECTOR-2}
```
public static int BENT_CONNECTOR_2
```


弯曲连接器 2.

### BENT_CONNECTOR_3 {#BENT-CONNECTOR-3}
```
public static int BENT_CONNECTOR_3
```


弯曲连接器 3.

### BENT_CONNECTOR_4 {#BENT-CONNECTOR-4}
```
public static int BENT_CONNECTOR_4
```


弯曲连接器 4.

### BENT_CONNECTOR_5 {#BENT-CONNECTOR-5}
```
public static int BENT_CONNECTOR_5
```


弯曲连接器 5.

### BENT_UP_ARROW {#BENT-UP-ARROW}
```
public static int BENT_UP_ARROW
```


向上弯曲箭头.

### BEVEL {#BEVEL}
```
public static int BEVEL
```


斜角.

### BLOCK_ARC {#BLOCK-ARC}
```
public static int BLOCK_ARC
```


块状弧形.

### BORDER_CALLOUT_1 {#BORDER-CALLOUT-1}
```
public static int BORDER_CALLOUT_1
```


带边框的标注 1.

### BORDER_CALLOUT_2 {#BORDER-CALLOUT-2}
```
public static int BORDER_CALLOUT_2
```


带边框的标注 2.

### BORDER_CALLOUT_3 {#BORDER-CALLOUT-3}
```
public static int BORDER_CALLOUT_3
```


带边框的标注 3.

### BRACE_PAIR {#BRACE-PAIR}
```
public static int BRACE_PAIR
```


大括号对.

### BRACKET_PAIR {#BRACKET-PAIR}
```
public static int BRACKET_PAIR
```


方括号对.

### CALLOUT_1 {#CALLOUT-1}
```
public static int CALLOUT_1
```


标注 1.

### CALLOUT_2 {#CALLOUT-2}
```
public static int CALLOUT_2
```


标注 2.

### CALLOUT_3 {#CALLOUT-3}
```
public static int CALLOUT_3
```


标注 3.

### CAN {#CAN}
```
public static int CAN
```


罐子.

### CHART_PLUS {#CHART-PLUS}
```
public static int CHART_PLUS
```


图表加号.

### CHART_STAR {#CHART-STAR}
```
public static int CHART_STAR
```


图表星形.

### CHART_X {#CHART-X}
```
public static int CHART_X
```


图表 X.

### CHEVRON {#CHEVRON}
```
public static int CHEVRON
```


人字形.

### CHORD {#CHORD}
```
public static int CHORD
```


弦.

### CIRCULAR_ARROW {#CIRCULAR-ARROW}
```
public static int CIRCULAR_ARROW
```


圆形箭头。

### CLOUD {#CLOUD}
```
public static int CLOUD
```


云形。

### CLOUD_CALLOUT {#CLOUD-CALLOUT}
```
public static int CLOUD_CALLOUT
```


云形标注。

### CORNER {#CORNER}
```
public static int CORNER
```


角形。

### CORNER_TABS {#CORNER-TABS}
```
public static int CORNER_TABS
```


角形标签。

### CUBE {#CUBE}
```
public static int CUBE
```


立方体。

### CURVED_CONNECTOR_2 {#CURVED-CONNECTOR-2}
```
public static int CURVED_CONNECTOR_2
```


弯曲连接线 2。

### CURVED_CONNECTOR_3 {#CURVED-CONNECTOR-3}
```
public static int CURVED_CONNECTOR_3
```


弯曲连接线 3。

### CURVED_CONNECTOR_4 {#CURVED-CONNECTOR-4}
```
public static int CURVED_CONNECTOR_4
```


弯曲连接线 4。

### CURVED_CONNECTOR_5 {#CURVED-CONNECTOR-5}
```
public static int CURVED_CONNECTOR_5
```


弯曲连接线 5。

### CURVED_DOWN_ARROW {#CURVED-DOWN-ARROW}
```
public static int CURVED_DOWN_ARROW
```


向下弯曲箭头。

### CURVED_LEFT_ARROW {#CURVED-LEFT-ARROW}
```
public static int CURVED_LEFT_ARROW
```


向左弯曲箭头。

### CURVED_RIGHT_ARROW {#CURVED-RIGHT-ARROW}
```
public static int CURVED_RIGHT_ARROW
```


向右弯曲箭头。

### CURVED_UP_ARROW {#CURVED-UP-ARROW}
```
public static int CURVED_UP_ARROW
```


向上弯曲箭头。

### DECAGON {#DECAGON}
```
public static int DECAGON
```


十边形。

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


指示图表元素未定义形状。

### DIAGONAL_CORNERS_ROUNDED {#DIAGONAL-CORNERS-ROUNDED}
```
public static int DIAGONAL_CORNERS_ROUNDED
```


圆角对角矩形。

### DIAGONAL_CORNERS_SNIPPED {#DIAGONAL-CORNERS-SNIPPED}
```
public static int DIAGONAL_CORNERS_SNIPPED
```


斜切对角矩形。

### DIAGONAL_STRIPE {#DIAGONAL-STRIPE}
```
public static int DIAGONAL_STRIPE
```


对角条纹。

### DIAMOND {#DIAMOND}
```
public static int DIAMOND
```


菱形。

### DODECAGON {#DODECAGON}
```
public static int DODECAGON
```


十二边形。

### DONUT {#DONUT}
```
public static int DONUT
```


环形。

### DOUBLE_WAVE {#DOUBLE-WAVE}
```
public static int DOUBLE_WAVE
```


双波形。

### DOWN_ARROW {#DOWN-ARROW}
```
public static int DOWN_ARROW
```


向下箭头。

### DOWN_ARROW_CALLOUT {#DOWN-ARROW-CALLOUT}
```
public static int DOWN_ARROW_CALLOUT
```


向下标注箭头。

### ELLIPSE {#ELLIPSE}
```
public static int ELLIPSE
```


椭圆.

### ELLIPSE_RIBBON {#ELLIPSE-RIBBON}
```
public static int ELLIPSE_RIBBON
```


椭圆带.

### ELLIPSE_RIBBON_2 {#ELLIPSE-RIBBON-2}
```
public static int ELLIPSE_RIBBON_2
```


椭圆带 2.

### FLOW_CHART_ALTERNATE_PROCESS {#FLOW-CHART-ALTERNATE-PROCESS}
```
public static int FLOW_CHART_ALTERNATE_PROCESS
```


交替流程.

### FLOW_CHART_COLLATE {#FLOW-CHART-COLLATE}
```
public static int FLOW_CHART_COLLATE
```


汇总流程.

### FLOW_CHART_CONNECTOR {#FLOW-CHART-CONNECTOR}
```
public static int FLOW_CHART_CONNECTOR
```


连接器流程.

### FLOW_CHART_DECISION {#FLOW-CHART-DECISION}
```
public static int FLOW_CHART_DECISION
```


决策流程.

### FLOW_CHART_DELAY {#FLOW-CHART-DELAY}
```
public static int FLOW_CHART_DELAY
```


延迟流程.

### FLOW_CHART_DISPLAY {#FLOW-CHART-DISPLAY}
```
public static int FLOW_CHART_DISPLAY
```


显示流程.

### FLOW_CHART_DOCUMENT {#FLOW-CHART-DOCUMENT}
```
public static int FLOW_CHART_DOCUMENT
```


文档流程.

### FLOW_CHART_EXTRACT {#FLOW-CHART-EXTRACT}
```
public static int FLOW_CHART_EXTRACT
```


提取流程.

### FLOW_CHART_INPUT_OUTPUT {#FLOW-CHART-INPUT-OUTPUT}
```
public static int FLOW_CHART_INPUT_OUTPUT
```


输入输出流程.

### FLOW_CHART_INTERNAL_STORAGE {#FLOW-CHART-INTERNAL-STORAGE}
```
public static int FLOW_CHART_INTERNAL_STORAGE
```


内部存储流程.

### FLOW_CHART_MAGNETIC_DISK {#FLOW-CHART-MAGNETIC-DISK}
```
public static int FLOW_CHART_MAGNETIC_DISK
```


磁盘流程.

### FLOW_CHART_MAGNETIC_DRUM {#FLOW-CHART-MAGNETIC-DRUM}
```
public static int FLOW_CHART_MAGNETIC_DRUM
```


磁鼓流程.

### FLOW_CHART_MAGNETIC_TAPE {#FLOW-CHART-MAGNETIC-TAPE}
```
public static int FLOW_CHART_MAGNETIC_TAPE
```


磁带流程.

### FLOW_CHART_MANUAL_INPUT {#FLOW-CHART-MANUAL-INPUT}
```
public static int FLOW_CHART_MANUAL_INPUT
```


手动输入流程.

### FLOW_CHART_MANUAL_OPERATION {#FLOW-CHART-MANUAL-OPERATION}
```
public static int FLOW_CHART_MANUAL_OPERATION
```


手动操作流程.

### FLOW_CHART_MERGE {#FLOW-CHART-MERGE}
```
public static int FLOW_CHART_MERGE
```


合并流程.

### FLOW_CHART_MULTIDOCUMENT {#FLOW-CHART-MULTIDOCUMENT}
```
public static int FLOW_CHART_MULTIDOCUMENT
```


多文档流程.

### FLOW_CHART_OFFLINE_STORAGE {#FLOW-CHART-OFFLINE-STORAGE}
```
public static int FLOW_CHART_OFFLINE_STORAGE
```


离线存储流程.

### FLOW_CHART_OFFPAGE_CONNECTOR {#FLOW-CHART-OFFPAGE-CONNECTOR}
```
public static int FLOW_CHART_OFFPAGE_CONNECTOR
```


页外连接器流程.

### FLOW_CHART_ONLINE_STORAGE {#FLOW-CHART-ONLINE-STORAGE}
```
public static int FLOW_CHART_ONLINE_STORAGE
```


在线存储流程.

### FLOW_CHART_OR {#FLOW-CHART-OR}
```
public static int FLOW_CHART_OR
```


或流程.

### FLOW_CHART_PREDEFINED_PROCESS {#FLOW-CHART-PREDEFINED-PROCESS}
```
public static int FLOW_CHART_PREDEFINED_PROCESS
```


预定义流程.

### FLOW_CHART_PREPARATION {#FLOW-CHART-PREPARATION}
```
public static int FLOW_CHART_PREPARATION
```


准备流程。

### FLOW_CHART_PROCESS {#FLOW-CHART-PROCESS}
```
public static int FLOW_CHART_PROCESS
```


处理流程。

### FLOW_CHART_PUNCHED_CARD {#FLOW-CHART-PUNCHED-CARD}
```
public static int FLOW_CHART_PUNCHED_CARD
```


穿孔卡片流程。

### FLOW_CHART_PUNCHED_TAPE {#FLOW-CHART-PUNCHED-TAPE}
```
public static int FLOW_CHART_PUNCHED_TAPE
```


穿孔纸带流程。

### FLOW_CHART_SORT {#FLOW-CHART-SORT}
```
public static int FLOW_CHART_SORT
```


排序流程。

### FLOW_CHART_SUMMING_JUNCTION {#FLOW-CHART-SUMMING-JUNCTION}
```
public static int FLOW_CHART_SUMMING_JUNCTION
```


求和节点流程。

### FLOW_CHART_TERMINATOR {#FLOW-CHART-TERMINATOR}
```
public static int FLOW_CHART_TERMINATOR
```


终止符流程。

### FOLDED_CORNER {#FOLDED-CORNER}
```
public static int FOLDED_CORNER
```


折叠角。

### FRAME {#FRAME}
```
public static int FRAME
```


框架。

### FUNNEL {#FUNNEL}
```
public static int FUNNEL
```


漏斗。

### GEAR_6 {#GEAR-6}
```
public static int GEAR_6
```


六齿齿轮。

### GEAR_9 {#GEAR-9}
```
public static int GEAR_9
```


九齿齿轮。

### HALF_FRAME {#HALF-FRAME}
```
public static int HALF_FRAME
```


半框架。

### HEART {#HEART}
```
public static int HEART
```


心形。

### HEPTAGON {#HEPTAGON}
```
public static int HEPTAGON
```


七边形。

### HEXAGON {#HEXAGON}
```
public static int HEXAGON
```


六边形。

### HOME_PLATE {#HOME-PLATE}
```
public static int HOME_PLATE
```


本垒。

### HORIZONTAL_SCROLL {#HORIZONTAL-SCROLL}
```
public static int HORIZONTAL_SCROLL
```


水平滚动。

### INVERSE_LINE {#INVERSE-LINE}
```
public static int INVERSE_LINE
```


反向线。

### IRREGULAR_SEAL_1 {#IRREGULAR-SEAL-1}
```
public static int IRREGULAR_SEAL_1
```


不规则密封 1。

### IRREGULAR_SEAL_2 {#IRREGULAR-SEAL-2}
```
public static int IRREGULAR_SEAL_2
```


不规则密封 2。

### LEFT_ARROW {#LEFT-ARROW}
```
public static int LEFT_ARROW
```


左箭头。

### LEFT_ARROW_CALLOUT {#LEFT-ARROW-CALLOUT}
```
public static int LEFT_ARROW_CALLOUT
```


标注左箭头。

### LEFT_BRACE {#LEFT-BRACE}
```
public static int LEFT_BRACE
```


左大括号。

### LEFT_BRACKET {#LEFT-BRACKET}
```
public static int LEFT_BRACKET
```


左方括号。

### LEFT_CIRCULAR_ARROW {#LEFT-CIRCULAR-ARROW}
```
public static int LEFT_CIRCULAR_ARROW
```


左循环箭头。

### LEFT_RIGHT_ARROW {#LEFT-RIGHT-ARROW}
```
public static int LEFT_RIGHT_ARROW
```


左和右箭头。

### LEFT_RIGHT_ARROW_CALLOUT {#LEFT-RIGHT-ARROW-CALLOUT}
```
public static int LEFT_RIGHT_ARROW_CALLOUT
```


标注左和右箭头。

### LEFT_RIGHT_CIRCULAR_ARROW {#LEFT-RIGHT-CIRCULAR-ARROW}
```
public static int LEFT_RIGHT_CIRCULAR_ARROW
```


左右循环箭头。

### LEFT_RIGHT_RIBBON {#LEFT-RIGHT-RIBBON}
```
public static int LEFT_RIGHT_RIBBON
```


左右丝带。

### LEFT_RIGHT_UP_ARROW {#LEFT-RIGHT-UP-ARROW}
```
public static int LEFT_RIGHT_UP_ARROW
```


左右向上箭头。

### LEFT_UP_ARROW {#LEFT-UP-ARROW}
```
public static int LEFT_UP_ARROW
```


左上箭头。

### LIGHTNING_BOLT {#LIGHTNING-BOLT}
```
public static int LIGHTNING_BOLT
```


闪电。

### LINE {#LINE}
```
public static int LINE
```


线条。

### MATH_DIVIDE {#MATH-DIVIDE}
```
public static int MATH_DIVIDE
```


数学除号。

### MATH_EQUAL {#MATH-EQUAL}
```
public static int MATH_EQUAL
```


数学等号。

### MATH_MINUS {#MATH-MINUS}
```
public static int MATH_MINUS
```


数学减号。

### MATH_MULTIPLY {#MATH-MULTIPLY}
```
public static int MATH_MULTIPLY
```


数学乘号。

### MATH_NOT_EQUAL {#MATH-NOT-EQUAL}
```
public static int MATH_NOT_EQUAL
```


数学不等号。

### MATH_PLUS {#MATH-PLUS}
```
public static int MATH_PLUS
```


数学加号。

### MOON {#MOON}
```
public static int MOON
```


月亮。

### NON_ISOSCELES_TRAPEZOID {#NON-ISOSCELES-TRAPEZOID}
```
public static int NON_ISOSCELES_TRAPEZOID
```


非等腰梯形。

### NOTCHED_RIGHT_ARROW {#NOTCHED-RIGHT-ARROW}
```
public static int NOTCHED_RIGHT_ARROW
```


缺口右箭头。

### NO_SMOKING {#NO-SMOKING}
```
public static int NO_SMOKING
```


禁止吸烟。

### OCTAGON {#OCTAGON}
```
public static int OCTAGON
```


八边形。

### PARALLELOGRAM {#PARALLELOGRAM}
```
public static int PARALLELOGRAM
```


平行四边形。

### PENTAGON {#PENTAGON}
```
public static int PENTAGON
```


五边形。

### PIE {#PIE}
```
public static int PIE
```


饼图。

### PLAQUE {#PLAQUE}
```
public static int PLAQUE
```


牌匾。

### PLAQUE_TABS {#PLAQUE-TABS}
```
public static int PLAQUE_TABS
```


牌匾标签。

### PLUS {#PLUS}
```
public static int PLUS
```


加号。

### QUAD_ARROW {#QUAD-ARROW}
```
public static int QUAD_ARROW
```


四向箭头。

### QUAD_ARROW_CALLOUT {#QUAD-ARROW-CALLOUT}
```
public static int QUAD_ARROW_CALLOUT
```


注释四向箭头。

### RECTANGLE {#RECTANGLE}
```
public static int RECTANGLE
```


矩形。

### RIBBON {#RIBBON}
```
public static int RIBBON
```


丝带。

### RIBBON_2 {#RIBBON-2}
```
public static int RIBBON_2
```


丝带 2。

### RIGHT_ARROW_CALLOUT {#RIGHT-ARROW-CALLOUT}
```
public static int RIGHT_ARROW_CALLOUT
```


注释右箭头。

### RIGHT_BRACE {#RIGHT-BRACE}
```
public static int RIGHT_BRACE
```


右大括号。

### RIGHT_BRACKET {#RIGHT-BRACKET}
```
public static int RIGHT_BRACKET
```


右方括号。

### RIGHT_TRIANGLE {#RIGHT-TRIANGLE}
```
public static int RIGHT_TRIANGLE
```


直角三角形。

### ROUND_RECTANGLE {#ROUND-RECTANGLE}
```
public static int ROUND_RECTANGLE
```


圆角矩形。

### SEAL_10 {#SEAL-10}
```
public static int SEAL_10
```


十角星。

### SEAL_12 {#SEAL-12}
```
public static int SEAL_12
```


十二角星。

### SEAL_16 {#SEAL-16}
```
public static int SEAL_16
```


十六角星。

### SEAL_24 {#SEAL-24}
```
public static int SEAL_24
```


二十四角星。

### SEAL_32 {#SEAL-32}
```
public static int SEAL_32
```


三十二角星。

### SEAL_4 {#SEAL-4}
```
public static int SEAL_4
```


四角星。

### SEAL_6 {#SEAL-6}
```
public static int SEAL_6
```


六角星。

### SEAL_7 {#SEAL-7}
```
public static int SEAL_7
```


七角星。

### SEAL_8 {#SEAL-8}
```
public static int SEAL_8
```


八角星。

### SINGLE_CORNER_ROUNDED {#SINGLE-CORNER-ROUNDED}
```
public static int SINGLE_CORNER_ROUNDED
```


单角圆角矩形。

### SINGLE_CORNER_SNIPPED {#SINGLE-CORNER-SNIPPED}
```
public static int SINGLE_CORNER_SNIPPED
```


剪切单角矩形对象。

### SMILEY_FACE {#SMILEY-FACE}
```
public static int SMILEY_FACE
```


笑脸。

### SQUARE_TABS {#SQUARE-TABS}
```
public static int SQUARE_TABS
```


方形标签。

### STAR {#STAR}
```
public static int STAR
```


星形。

### STRAIGHT_CONNECTOR_1 {#STRAIGHT-CONNECTOR-1}
```
public static int STRAIGHT_CONNECTOR_1
```


直线连接器 1。

### STRIPED_RIGHT_ARROW {#STRIPED-RIGHT-ARROW}
```
public static int STRIPED_RIGHT_ARROW
```


条纹右箭头。

### SUN {#SUN}
```
public static int SUN
```


太阳。

### SWOOSH_ARROW {#SWOOSH-ARROW}
```
public static int SWOOSH_ARROW
```


弧形箭头。

### TEARDROP {#TEARDROP}
```
public static int TEARDROP
```


泪滴形。

### TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED {#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED}
```
public static int TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED
```


剪切并圆角单角矩形。

### TOP_CORNERS_ROUNDED {#TOP-CORNERS-ROUNDED}
```
public static int TOP_CORNERS_ROUNDED
```


同侧圆角矩形。

### TOP_CORNERS_SNIPPED {#TOP-CORNERS-SNIPPED}
```
public static int TOP_CORNERS_SNIPPED
```


同侧剪切角矩形。

### TRAPEZOID {#TRAPEZOID}
```
public static int TRAPEZOID
```


梯形。

### TRIANGLE {#TRIANGLE}
```
public static int TRIANGLE
```


三角形。

### UP_ARROW {#UP-ARROW}
```
public static int UP_ARROW
```


向上箭头。

### UP_ARROW_CALLOUT {#UP-ARROW-CALLOUT}
```
public static int UP_ARROW_CALLOUT
```


标注向上箭头。

### UP_DOWN_ARROW {#UP-DOWN-ARROW}
```
public static int UP_DOWN_ARROW
```


上下箭头。

### UP_DOWN_ARROW_CALLOUT {#UP-DOWN-ARROW-CALLOUT}
```
public static int UP_DOWN_ARROW_CALLOUT
```


标注上下箭头。

### UTURN_ARROW {#UTURN-ARROW}
```
public static int UTURN_ARROW
```


U形转弯箭头。

### VERTICAL_SCROLL {#VERTICAL-SCROLL}
```
public static int VERTICAL_SCROLL
```


垂直滚动。

### WAVE {#WAVE}
```
public static int WAVE
```


波形。

### WEDGE_ELLIPSE_CALLOUT {#WEDGE-ELLIPSE-CALLOUT}
```
public static int WEDGE_ELLIPSE_CALLOUT
```


标注楔形椭圆。

### WEDGE_PIE {#WEDGE-PIE}
```
public static int WEDGE_PIE
```


楔形饼图。

### WEDGE_RECT_CALLOUT {#WEDGE-RECT-CALLOUT}
```
public static int WEDGE_RECT_CALLOUT
```


标注楔形矩形。

### WEDGE_R_RECT_CALLOUT {#WEDGE-R-RECT-CALLOUT}
```
public static int WEDGE_R_RECT_CALLOUT
```


标注楔形圆角矩形。

### length {#length}
```
public static int length
```


### fromName(String chartShapeTypeName) {#fromName-java.lang.String}
```
public static int fromName(String chartShapeTypeName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| chartShapeTypeName | java.lang.String |  |

**Returns:**
int
### getName(int chartShapeType) {#getName-int}
```
public static String getName(int chartShapeType)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| chartShapeType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int chartShapeType) {#toString-int}
```
public static String toString(int chartShapeType)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| chartShapeType | int |  |

**Returns:**
java.lang.String
