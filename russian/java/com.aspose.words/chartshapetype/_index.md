---
title: "ChartShapeType"
linktitle: "ChartShapeType"
second_title: "Aspose.Words для Java"
description: "Указывает тип формы элементов диаграммы в Java."
type: docs
weight: 90
url: /ru/java/com.aspose.words/chartshapetype/
---

**Inheritance:**
java.lang.Object
```
public class ChartShapeType
```

Указывает тип формы элементов диаграммы.

 **Examples:** 

Показывает, как задать заполнение, обводку и форматирование выноски для меток данных диаграммы.

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
## Поля

| Поле | Описание |
| --- | --- |
| [ACCENT_BORDER_CALLOUT_1](#ACCENT-BORDER-CALLOUT-1) | Выноска с акцентом и границей 1. |
| [ACCENT_BORDER_CALLOUT_2](#ACCENT-BORDER-CALLOUT-2) | Выноска с акцентом и границей 2. |
| [ACCENT_BORDER_CALLOUT_3](#ACCENT-BORDER-CALLOUT-3) | Выноска с акцентом и границей 3. |
| [ACCENT_CALLOUT_1](#ACCENT-CALLOUT-1) | Выноска с акцентом 1. |
| [ACCENT_CALLOUT_2](#ACCENT-CALLOUT-2) | Выноска с акцентом 2. |
| [ACCENT_CALLOUT_3](#ACCENT-CALLOUT-3) | Выноска с акцентом 3. |
| [ACTION_BUTTON_BACK_PREVIOUS](#ACTION-BUTTON-BACK-PREVIOUS) | Кнопка «Назад» или «Предыдущая». |
| [ACTION_BUTTON_BEGINNING](#ACTION-BUTTON-BEGINNING) | Кнопка «Начало». |
| [ACTION_BUTTON_BLANK](#ACTION-BUTTON-BLANK) | Пустая кнопка. |
| [ACTION_BUTTON_DOCUMENT](#ACTION-BUTTON-DOCUMENT) | Кнопка «Документ». |
| [ACTION_BUTTON_END](#ACTION-BUTTON-END) | Кнопка «Конец». |
| [ACTION_BUTTON_FORWARD_NEXT](#ACTION-BUTTON-FORWARD-NEXT) | Кнопка «Вперёд» или «Следующая». |
| [ACTION_BUTTON_HELP](#ACTION-BUTTON-HELP) | Кнопка «Справка». |
| [ACTION_BUTTON_HOME](#ACTION-BUTTON-HOME) | Кнопка «Главная». |
| [ACTION_BUTTON_INFORMATION](#ACTION-BUTTON-INFORMATION) | Кнопка «Информация». |
| [ACTION_BUTTON_MOVIE](#ACTION-BUTTON-MOVIE) | Кнопка «Видео». |
| [ACTION_BUTTON_RETURN](#ACTION-BUTTON-RETURN) | Кнопка «Возврат». |
| [ACTION_BUTTON_SOUND](#ACTION-BUTTON-SOUND) | Кнопка «Звук». |
| [ARC](#ARC) | Дуга. |
| [ARROW](#ARROW) | Стрелка. |
| [BENT_ARROW](#BENT-ARROW) | Согнутая стрелка. |
| [BENT_CONNECTOR_2](#BENT-CONNECTOR-2) | Согнутый соединитель 2. |
| [BENT_CONNECTOR_3](#BENT-CONNECTOR-3) | Согнутый соединитель 3. |
| [BENT_CONNECTOR_4](#BENT-CONNECTOR-4) | Согнутый соединитель 4. |
| [BENT_CONNECTOR_5](#BENT-CONNECTOR-5) | Согнутый соединитель 5. |
| [BENT_UP_ARROW](#BENT-UP-ARROW) | Согнутая стрелка вверх. |
| [BEVEL](#BEVEL) | Скос. |
| [BLOCK_ARC](#BLOCK-ARC) | Блочная дуга. |
| [BORDER_CALLOUT_1](#BORDER-CALLOUT-1) | Врезка с рамкой 1. |
| [BORDER_CALLOUT_2](#BORDER-CALLOUT-2) | Врезка с рамкой 2. |
| [BORDER_CALLOUT_3](#BORDER-CALLOUT-3) | Врезка с рамкой 3. |
| [BRACE_PAIR](#BRACE-PAIR) | Парные фигурные скобки. |
| [BRACKET_PAIR](#BRACKET-PAIR) | Парные квадратные скобки. |
| [CALLOUT_1](#CALLOUT-1) | Врезка 1. |
| [CALLOUT_2](#CALLOUT-2) | Врезка 2. |
| [CALLOUT_3](#CALLOUT-3) | Врезка 3. |
| [CAN](#CAN) | Банка. |
| [CHART_PLUS](#CHART-PLUS) | Диаграмма плюс. |
| [CHART_STAR](#CHART-STAR) | Диаграмма звезда. |
| [CHART_X](#CHART-X) | Диаграмма X. |
| [CHEVRON](#CHEVRON) | Шеврон. |
| [CHORD](#CHORD) | Хорда. |
| [CIRCULAR_ARROW](#CIRCULAR-ARROW) | Круговая стрелка. |
| [CLOUD](#CLOUD) | Облако. |
| [CLOUD_CALLOUT](#CLOUD-CALLOUT) | Врезка облако. |
| [CORNER](#CORNER) | Угол. |
| [CORNER_TABS](#CORNER-TABS) | Угловые вкладки. |
| [CUBE](#CUBE) | Куб. |
| [CURVED_CONNECTOR_2](#CURVED-CONNECTOR-2) | Изогнутый соединитель 2. |
| [CURVED_CONNECTOR_3](#CURVED-CONNECTOR-3) | Изогнутый соединитель 3. |
| [CURVED_CONNECTOR_4](#CURVED-CONNECTOR-4) | Изогнутый соединитель 4. |
| [CURVED_CONNECTOR_5](#CURVED-CONNECTOR-5) | Изогнутый соединитель 5. |
| [CURVED_DOWN_ARROW](#CURVED-DOWN-ARROW) | Изогнутая стрелка вниз. |
| [CURVED_LEFT_ARROW](#CURVED-LEFT-ARROW) | Изогнутая стрелка влево. |
| [CURVED_RIGHT_ARROW](#CURVED-RIGHT-ARROW) | Изогнутая стрелка вправо. |
| [CURVED_UP_ARROW](#CURVED-UP-ARROW) | Изогнутая стрелка вверх. |
| [DECAGON](#DECAGON) | Десятиугольник. |
| [DEFAULT](#DEFAULT) | Указывает, что форма не определена для элемента диаграммы. |
| [DIAGONAL_CORNERS_ROUNDED](#DIAGONAL-CORNERS-ROUNDED) | Прямоугольник с закруглённым диагональным углом. |
| [DIAGONAL_CORNERS_SNIPPED](#DIAGONAL-CORNERS-SNIPPED) | Прямоугольник с отрезанным диагональным углом. |
| [DIAGONAL_STRIPE](#DIAGONAL-STRIPE) | Диагональная полоса. |
| [DIAMOND](#DIAMOND) | Ромб. |
| [DODECAGON](#DODECAGON) | Двенадцатиугольник. |
| [DONUT](#DONUT) | Кольцо. |
| [DOUBLE_WAVE](#DOUBLE-WAVE) | Двойная волна. |
| [DOWN_ARROW](#DOWN-ARROW) | Стрелка вниз. |
| [DOWN_ARROW_CALLOUT](#DOWN-ARROW-CALLOUT) | Врезка со стрелкой вниз. |
| [ELLIPSE](#ELLIPSE) | Эллипс. |
| [ELLIPSE_RIBBON](#ELLIPSE-RIBBON) | Эллиптическая лента. |
| [ELLIPSE_RIBBON_2](#ELLIPSE-RIBBON-2) | Эллиптическая лента 2. |
| [FLOW_CHART_ALTERNATE_PROCESS](#FLOW-CHART-ALTERNATE-PROCESS) | Альтернативный процессный поток. |
| [FLOW_CHART_COLLATE](#FLOW-CHART-COLLATE) | Поток сопоставления. |
| [FLOW_CHART_CONNECTOR](#FLOW-CHART-CONNECTOR) | Поток соединителя. |
| [FLOW_CHART_DECISION](#FLOW-CHART-DECISION) | Поток принятия решения. |
| [FLOW_CHART_DELAY](#FLOW-CHART-DELAY) | Поток задержки. |
| [FLOW_CHART_DISPLAY](#FLOW-CHART-DISPLAY) | Поток отображения. |
| [FLOW_CHART_DOCUMENT](#FLOW-CHART-DOCUMENT) | Поток документа. |
| [FLOW_CHART_EXTRACT](#FLOW-CHART-EXTRACT) | Поток извлечения. |
| [FLOW_CHART_INPUT_OUTPUT](#FLOW-CHART-INPUT-OUTPUT) | Поток ввода-вывода. |
| [FLOW_CHART_INTERNAL_STORAGE](#FLOW-CHART-INTERNAL-STORAGE) | Поток внутреннего хранилища. |
| [FLOW_CHART_MAGNETIC_DISK](#FLOW-CHART-MAGNETIC-DISK) | Поток магнитного диска. |
| [FLOW_CHART_MAGNETIC_DRUM](#FLOW-CHART-MAGNETIC-DRUM) | Поток магнитного барабана. |
| [FLOW_CHART_MAGNETIC_TAPE](#FLOW-CHART-MAGNETIC-TAPE) | Поток магнитной ленты. |
| [FLOW_CHART_MANUAL_INPUT](#FLOW-CHART-MANUAL-INPUT) | Поток ручного ввода. |
| [FLOW_CHART_MANUAL_OPERATION](#FLOW-CHART-MANUAL-OPERATION) | Поток ручной операции. |
| [FLOW_CHART_MERGE](#FLOW-CHART-MERGE) | Поток слияния. |
| [FLOW_CHART_MULTIDOCUMENT](#FLOW-CHART-MULTIDOCUMENT) | Поток многодокументный. |
| [FLOW_CHART_OFFLINE_STORAGE](#FLOW-CHART-OFFLINE-STORAGE) | Поток офлайн-хранилища. |
| [FLOW_CHART_OFFPAGE_CONNECTOR](#FLOW-CHART-OFFPAGE-CONNECTOR) | Поток соединителя вне страницы. |
| [FLOW_CHART_ONLINE_STORAGE](#FLOW-CHART-ONLINE-STORAGE) | Поток онлайн-хранилища. |
| [FLOW_CHART_OR](#FLOW-CHART-OR) | Поток ИЛИ. |
| [FLOW_CHART_PREDEFINED_PROCESS](#FLOW-CHART-PREDEFINED-PROCESS) | Поток предопределённого процесса. |
| [FLOW_CHART_PREPARATION](#FLOW-CHART-PREPARATION) | Поток подготовки. |
| [FLOW_CHART_PROCESS](#FLOW-CHART-PROCESS) | Поток процесса. |
| [FLOW_CHART_PUNCHED_CARD](#FLOW-CHART-PUNCHED-CARD) | Поток перфокарты. |
| [FLOW_CHART_PUNCHED_TAPE](#FLOW-CHART-PUNCHED-TAPE) | Поток перфорированной ленты. |
| [FLOW_CHART_SORT](#FLOW-CHART-SORT) | Поток сортировки. |
| [FLOW_CHART_SUMMING_JUNCTION](#FLOW-CHART-SUMMING-JUNCTION) | Поток суммирующего узла. |
| [FLOW_CHART_TERMINATOR](#FLOW-CHART-TERMINATOR) | Поток терминатора. |
| [FOLDED_CORNER](#FOLDED-CORNER) | Сложенный угол. |
| [FRAME](#FRAME) | Рамка. |
| [FUNNEL](#FUNNEL) | Воронка. |
| [GEAR_6](#GEAR-6) | Шестерня с шестью зубьями. |
| [GEAR_9](#GEAR-9) | Шестерня с девятью зубьями. |
| [HALF_FRAME](#HALF-FRAME) | Полурама. |
| [HEART](#HEART) | Сердце. |
| [HEPTAGON](#HEPTAGON) | Семигранник. |
| [HEXAGON](#HEXAGON) | Шестиугольник. |
| [HOME_PLATE](#HOME-PLATE) | Домашняя плита. |
| [HORIZONTAL_SCROLL](#HORIZONTAL-SCROLL) | Горизонтальная прокрутка. |
| [INVERSE_LINE](#INVERSE-LINE) | Обратная линия. |
| [IRREGULAR_SEAL_1](#IRREGULAR-SEAL-1) | Нерегулярное уплотнение 1. |
| [IRREGULAR_SEAL_2](#IRREGULAR-SEAL-2) | Нерегулярное уплотнение 2. |
| [LEFT_ARROW](#LEFT-ARROW) | Стрелка влево. |
| [LEFT_ARROW_CALLOUT](#LEFT-ARROW-CALLOUT) | Выноска со стрелкой влево. |
| [LEFT_BRACE](#LEFT-BRACE) | Левая фигурная скобка. |
| [LEFT_BRACKET](#LEFT-BRACKET) | Левая квадратная скобка. |
| [LEFT_CIRCULAR_ARROW](#LEFT-CIRCULAR-ARROW) | Левая круговая стрелка. |
| [LEFT_RIGHT_ARROW](#LEFT-RIGHT-ARROW) | Стрелка влево и вправо. |
| [LEFT_RIGHT_ARROW_CALLOUT](#LEFT-RIGHT-ARROW-CALLOUT) | Выноска со стрелкой влево и вправо. |
| [LEFT_RIGHT_CIRCULAR_ARROW](#LEFT-RIGHT-CIRCULAR-ARROW) | Круговая стрелка слева направо. |
| [LEFT_RIGHT_RIBBON](#LEFT-RIGHT-RIBBON) | Лента слева направо. |
| [LEFT_RIGHT_UP_ARROW](#LEFT-RIGHT-UP-ARROW) | Стрелка влево‑вправо‑вверх. |
| [LEFT_UP_ARROW](#LEFT-UP-ARROW) | Стрелка влево‑вверх. |
| [LIGHTNING_BOLT](#LIGHTNING-BOLT) | Молния. |
| [LINE](#LINE) | Линия. |
| [MATH_DIVIDE](#MATH-DIVIDE) | Знак деления. |
| [MATH_EQUAL](#MATH-EQUAL) | Знак равенства. |
| [MATH_MINUS](#MATH-MINUS) | Знак вычитания. |
| [MATH_MULTIPLY](#MATH-MULTIPLY) | Знак умножения. |
| [MATH_NOT_EQUAL](#MATH-NOT-EQUAL) | Знак неравенства. |
| [MATH_PLUS](#MATH-PLUS) | Знак сложения. |
| [MOON](#MOON) | Луна. |
| [NON_ISOSCELES_TRAPEZOID](#NON-ISOSCELES-TRAPEZOID) | Неравнобедренная трапеция. |
| [NOTCHED_RIGHT_ARROW](#NOTCHED-RIGHT-ARROW) | Стрелка вправо с вырезом. |
| [NO_SMOKING](#NO-SMOKING) | Запрет курения. |
| [OCTAGON](#OCTAGON) | Восьмиугольник. |
| [PARALLELOGRAM](#PARALLELOGRAM) | Параллелограмм. |
| [PENTAGON](#PENTAGON) | Пятиугольник. |
| [PIE](#PIE) | Круговая диаграмма. |
| [PLAQUE](#PLAQUE) | Табличка. |
| [PLAQUE_TABS](#PLAQUE-TABS) | Вкладки таблички. |
| [PLUS](#PLUS) | Плюс. |
| [QUAD_ARROW](#QUAD-ARROW) | Стрелка в четыре стороны. |
| [QUAD_ARROW_CALLOUT](#QUAD-ARROW-CALLOUT) | Выноска с четырёхстрелкой. |
| [RECTANGLE](#RECTANGLE) | Прямоугольник. |
| [RIBBON](#RIBBON) | Лента. |
| [RIBBON_2](#RIBBON-2) | Лента 2. |
| [RIGHT_ARROW_CALLOUT](#RIGHT-ARROW-CALLOUT) | Врезка со стрелкой вправо. |
| [RIGHT_BRACE](#RIGHT-BRACE) | Правая фигурная скобка. |
| [RIGHT_BRACKET](#RIGHT-BRACKET) | Правая квадратная скобка. |
| [RIGHT_TRIANGLE](#RIGHT-TRIANGLE) | Правый треугольник. |
| [ROUND_RECTANGLE](#ROUND-RECTANGLE) | Скруглённый прямоугольник. |
| [SEAL_10](#SEAL-10) | Звезда с десятью лучами. |
| [SEAL_12](#SEAL-12) | Звезда с двенадцатью лучами. |
| [SEAL_16](#SEAL-16) | Звезда с шестнадцатью лучами. |
| [SEAL_24](#SEAL-24) | Звезда с двадцатью четырьмя лучами. |
| [SEAL_32](#SEAL-32) | Звезда с тридцатью двумя лучами. |
| [SEAL_4](#SEAL-4) | Звезда с четырьмя лучами. |
| [SEAL_6](#SEAL-6) | Звезда с шестью лучами. |
| [SEAL_7](#SEAL-7) | Звезда с семью лучами. |
| [SEAL_8](#SEAL-8) | Звезда с восемью лучами. |
| [SINGLE_CORNER_ROUNDED](#SINGLE-CORNER-ROUNDED) | Скруглённый прямоугольник с одной скруглённой стороной. |
| [SINGLE_CORNER_SNIPPED](#SINGLE-CORNER-SNIPPED) | Объект с вырезанным углом у прямоугольника. |
| [SMILEY_FACE](#SMILEY-FACE) | Смайлик. |
| [SQUARE_TABS](#SQUARE-TABS) | Квадратные вкладки. |
| [STAR](#STAR) | Звезда. |
| [STRAIGHT_CONNECTOR_1](#STRAIGHT-CONNECTOR-1) | Прямой соединитель 1. |
| [STRIPED_RIGHT_ARROW](#STRIPED-RIGHT-ARROW) | Полосатая стрелка вправо. |
| [SUN](#SUN) | Солнце. |
| [SWOOSH_ARROW](#SWOOSH-ARROW) | Стрелка‑свисток. |
| [TEARDROP](#TEARDROP) | Капля. |
| [TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED](#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED) | Прямоугольник с отрезанным и скруглённым одним углом. |
| [TOP_CORNERS_ROUNDED](#TOP-CORNERS-ROUNDED) | Прямоугольник с округлым углом одной стороны. |
| [TOP_CORNERS_SNIPPED](#TOP-CORNERS-SNIPPED) | Прямоугольник с отрезанным углом одной стороны. |
| [TRAPEZOID](#TRAPEZOID) | Трапеция. |
| [TRIANGLE](#TRIANGLE) | Треугольник. |
| [UP_ARROW](#UP-ARROW) | Стрелка вверх. |
| [UP_ARROW_CALLOUT](#UP-ARROW-CALLOUT) | Выноска со стрелкой вверх. |
| [UP_DOWN_ARROW](#UP-DOWN-ARROW) | Стрелка вверх и вниз. |
| [UP_DOWN_ARROW_CALLOUT](#UP-DOWN-ARROW-CALLOUT) | Выноска со стрелкой вверх и вниз. |
| [UTURN_ARROW](#UTURN-ARROW) | Стрелка разворота. |
| [VERTICAL_SCROLL](#VERTICAL-SCROLL) | Вертикальная прокрутка. |
| [WAVE](#WAVE) | Волна. |
| [WEDGE_ELLIPSE_CALLOUT](#WEDGE-ELLIPSE-CALLOUT) | Выноска с сектором эллипса. |
| [WEDGE_PIE](#WEDGE-PIE) | Секторный круг. |
| [WEDGE_RECT_CALLOUT](#WEDGE-RECT-CALLOUT) | Выноска с сектором прямоугольника. |
| [WEDGE_R_RECT_CALLOUT](#WEDGE-R-RECT-CALLOUT) | Выноска с сектором скруглённого прямоугольника. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String chartShapeTypeName)](#fromName-java.lang.String) |  |
| [getName(int chartShapeType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartShapeType)](#toString-int) |  |
### ACCENT_BORDER_CALLOUT_1 {#ACCENT-BORDER-CALLOUT-1}
```
public static int ACCENT_BORDER_CALLOUT_1
```


Выноска с акцентом и границей 1.

### ACCENT_BORDER_CALLOUT_2 {#ACCENT-BORDER-CALLOUT-2}
```
public static int ACCENT_BORDER_CALLOUT_2
```


Выноска с акцентом и границей 2.

### ACCENT_BORDER_CALLOUT_3 {#ACCENT-BORDER-CALLOUT-3}
```
public static int ACCENT_BORDER_CALLOUT_3
```


Выноска с акцентом и границей 3.

### ACCENT_CALLOUT_1 {#ACCENT-CALLOUT-1}
```
public static int ACCENT_CALLOUT_1
```


Выноска с акцентом 1.

### ACCENT_CALLOUT_2 {#ACCENT-CALLOUT-2}
```
public static int ACCENT_CALLOUT_2
```


Выноска с акцентом 2.

### ACCENT_CALLOUT_3 {#ACCENT-CALLOUT-3}
```
public static int ACCENT_CALLOUT_3
```


Выноска с акцентом 3.

### ACTION_BUTTON_BACK_PREVIOUS {#ACTION-BUTTON-BACK-PREVIOUS}
```
public static int ACTION_BUTTON_BACK_PREVIOUS
```


Кнопка «Назад» или «Предыдущая».

### ACTION_BUTTON_BEGINNING {#ACTION-BUTTON-BEGINNING}
```
public static int ACTION_BUTTON_BEGINNING
```


Кнопка «Начало».

### ACTION_BUTTON_BLANK {#ACTION-BUTTON-BLANK}
```
public static int ACTION_BUTTON_BLANK
```


Пустая кнопка.

### ACTION_BUTTON_DOCUMENT {#ACTION-BUTTON-DOCUMENT}
```
public static int ACTION_BUTTON_DOCUMENT
```


Кнопка «Документ».

### ACTION_BUTTON_END {#ACTION-BUTTON-END}
```
public static int ACTION_BUTTON_END
```


Кнопка «Конец».

### ACTION_BUTTON_FORWARD_NEXT {#ACTION-BUTTON-FORWARD-NEXT}
```
public static int ACTION_BUTTON_FORWARD_NEXT
```


Кнопка «Вперёд» или «Следующая».

### ACTION_BUTTON_HELP {#ACTION-BUTTON-HELP}
```
public static int ACTION_BUTTON_HELP
```


Кнопка «Справка».

### ACTION_BUTTON_HOME {#ACTION-BUTTON-HOME}
```
public static int ACTION_BUTTON_HOME
```


Кнопка «Главная».

### ACTION_BUTTON_INFORMATION {#ACTION-BUTTON-INFORMATION}
```
public static int ACTION_BUTTON_INFORMATION
```


Кнопка «Информация».

### ACTION_BUTTON_MOVIE {#ACTION-BUTTON-MOVIE}
```
public static int ACTION_BUTTON_MOVIE
```


Кнопка «Видео».

### ACTION_BUTTON_RETURN {#ACTION-BUTTON-RETURN}
```
public static int ACTION_BUTTON_RETURN
```


Кнопка «Возврат».

### ACTION_BUTTON_SOUND {#ACTION-BUTTON-SOUND}
```
public static int ACTION_BUTTON_SOUND
```


Кнопка «Звук».

### ARC {#ARC}
```
public static int ARC
```


Дуга.

### ARROW {#ARROW}
```
public static int ARROW
```


Стрелка.

### BENT_ARROW {#BENT-ARROW}
```
public static int BENT_ARROW
```


Согнутая стрелка.

### BENT_CONNECTOR_2 {#BENT-CONNECTOR-2}
```
public static int BENT_CONNECTOR_2
```


Согнутый соединитель 2.

### BENT_CONNECTOR_3 {#BENT-CONNECTOR-3}
```
public static int BENT_CONNECTOR_3
```


Согнутый соединитель 3.

### BENT_CONNECTOR_4 {#BENT-CONNECTOR-4}
```
public static int BENT_CONNECTOR_4
```


Согнутый соединитель 4.

### BENT_CONNECTOR_5 {#BENT-CONNECTOR-5}
```
public static int BENT_CONNECTOR_5
```


Согнутый соединитель 5.

### BENT_UP_ARROW {#BENT-UP-ARROW}
```
public static int BENT_UP_ARROW
```


Согнутая стрелка вверх.

### BEVEL {#BEVEL}
```
public static int BEVEL
```


Скос.

### BLOCK_ARC {#BLOCK-ARC}
```
public static int BLOCK_ARC
```


Блочная дуга.

### BORDER_CALLOUT_1 {#BORDER-CALLOUT-1}
```
public static int BORDER_CALLOUT_1
```


Врезка с рамкой 1.

### BORDER_CALLOUT_2 {#BORDER-CALLOUT-2}
```
public static int BORDER_CALLOUT_2
```


Врезка с рамкой 2.

### BORDER_CALLOUT_3 {#BORDER-CALLOUT-3}
```
public static int BORDER_CALLOUT_3
```


Врезка с рамкой 3.

### BRACE_PAIR {#BRACE-PAIR}
```
public static int BRACE_PAIR
```


Парные фигурные скобки.

### BRACKET_PAIR {#BRACKET-PAIR}
```
public static int BRACKET_PAIR
```


Парные квадратные скобки.

### CALLOUT_1 {#CALLOUT-1}
```
public static int CALLOUT_1
```


Врезка 1.

### CALLOUT_2 {#CALLOUT-2}
```
public static int CALLOUT_2
```


Врезка 2.

### CALLOUT_3 {#CALLOUT-3}
```
public static int CALLOUT_3
```


Врезка 3.

### CAN {#CAN}
```
public static int CAN
```


Банка.

### CHART_PLUS {#CHART-PLUS}
```
public static int CHART_PLUS
```


Диаграмма плюс.

### CHART_STAR {#CHART-STAR}
```
public static int CHART_STAR
```


Диаграмма звезда.

### CHART_X {#CHART-X}
```
public static int CHART_X
```


Диаграмма X.

### CHEVRON {#CHEVRON}
```
public static int CHEVRON
```


Шеврон.

### CHORD {#CHORD}
```
public static int CHORD
```


Хорда.

### CIRCULAR_ARROW {#CIRCULAR-ARROW}
```
public static int CIRCULAR_ARROW
```


Круговая стрелка.

### CLOUD {#CLOUD}
```
public static int CLOUD
```


Облако.

### CLOUD_CALLOUT {#CLOUD-CALLOUT}
```
public static int CLOUD_CALLOUT
```


Врезка облако.

### CORNER {#CORNER}
```
public static int CORNER
```


Угол.

### CORNER_TABS {#CORNER-TABS}
```
public static int CORNER_TABS
```


Угловые вкладки.

### CUBE {#CUBE}
```
public static int CUBE
```


Куб.

### CURVED_CONNECTOR_2 {#CURVED-CONNECTOR-2}
```
public static int CURVED_CONNECTOR_2
```


Изогнутый соединитель 2.

### CURVED_CONNECTOR_3 {#CURVED-CONNECTOR-3}
```
public static int CURVED_CONNECTOR_3
```


Изогнутый соединитель 3.

### CURVED_CONNECTOR_4 {#CURVED-CONNECTOR-4}
```
public static int CURVED_CONNECTOR_4
```


Изогнутый соединитель 4.

### CURVED_CONNECTOR_5 {#CURVED-CONNECTOR-5}
```
public static int CURVED_CONNECTOR_5
```


Изогнутый соединитель 5.

### CURVED_DOWN_ARROW {#CURVED-DOWN-ARROW}
```
public static int CURVED_DOWN_ARROW
```


Изогнутая стрелка вниз.

### CURVED_LEFT_ARROW {#CURVED-LEFT-ARROW}
```
public static int CURVED_LEFT_ARROW
```


Изогнутая стрелка влево.

### CURVED_RIGHT_ARROW {#CURVED-RIGHT-ARROW}
```
public static int CURVED_RIGHT_ARROW
```


Изогнутая стрелка вправо.

### CURVED_UP_ARROW {#CURVED-UP-ARROW}
```
public static int CURVED_UP_ARROW
```


Изогнутая стрелка вверх.

### DECAGON {#DECAGON}
```
public static int DECAGON
```


Десятиугольник.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Указывает, что форма не определена для элемента диаграммы.

### DIAGONAL_CORNERS_ROUNDED {#DIAGONAL-CORNERS-ROUNDED}
```
public static int DIAGONAL_CORNERS_ROUNDED
```


Прямоугольник с закруглённым диагональным углом.

### DIAGONAL_CORNERS_SNIPPED {#DIAGONAL-CORNERS-SNIPPED}
```
public static int DIAGONAL_CORNERS_SNIPPED
```


Прямоугольник с отрезанным диагональным углом.

### DIAGONAL_STRIPE {#DIAGONAL-STRIPE}
```
public static int DIAGONAL_STRIPE
```


Диагональная полоса.

### DIAMOND {#DIAMOND}
```
public static int DIAMOND
```


Ромб.

### DODECAGON {#DODECAGON}
```
public static int DODECAGON
```


Двенадцатиугольник.

### DONUT {#DONUT}
```
public static int DONUT
```


Кольцо.

### DOUBLE_WAVE {#DOUBLE-WAVE}
```
public static int DOUBLE_WAVE
```


Двойная волна.

### DOWN_ARROW {#DOWN-ARROW}
```
public static int DOWN_ARROW
```


Стрелка вниз.

### DOWN_ARROW_CALLOUT {#DOWN-ARROW-CALLOUT}
```
public static int DOWN_ARROW_CALLOUT
```


Врезка со стрелкой вниз.

### ELLIPSE {#ELLIPSE}
```
public static int ELLIPSE
```


Эллипс.

### ELLIPSE_RIBBON {#ELLIPSE-RIBBON}
```
public static int ELLIPSE_RIBBON
```


Эллиптическая лента.

### ELLIPSE_RIBBON_2 {#ELLIPSE-RIBBON-2}
```
public static int ELLIPSE_RIBBON_2
```


Эллиптическая лента 2.

### FLOW_CHART_ALTERNATE_PROCESS {#FLOW-CHART-ALTERNATE-PROCESS}
```
public static int FLOW_CHART_ALTERNATE_PROCESS
```


Альтернативный процессный поток.

### FLOW_CHART_COLLATE {#FLOW-CHART-COLLATE}
```
public static int FLOW_CHART_COLLATE
```


Поток сопоставления.

### FLOW_CHART_CONNECTOR {#FLOW-CHART-CONNECTOR}
```
public static int FLOW_CHART_CONNECTOR
```


Поток соединителя.

### FLOW_CHART_DECISION {#FLOW-CHART-DECISION}
```
public static int FLOW_CHART_DECISION
```


Поток принятия решения.

### FLOW_CHART_DELAY {#FLOW-CHART-DELAY}
```
public static int FLOW_CHART_DELAY
```


Поток задержки.

### FLOW_CHART_DISPLAY {#FLOW-CHART-DISPLAY}
```
public static int FLOW_CHART_DISPLAY
```


Поток отображения.

### FLOW_CHART_DOCUMENT {#FLOW-CHART-DOCUMENT}
```
public static int FLOW_CHART_DOCUMENT
```


Поток документа.

### FLOW_CHART_EXTRACT {#FLOW-CHART-EXTRACT}
```
public static int FLOW_CHART_EXTRACT
```


Поток извлечения.

### FLOW_CHART_INPUT_OUTPUT {#FLOW-CHART-INPUT-OUTPUT}
```
public static int FLOW_CHART_INPUT_OUTPUT
```


Поток ввода-вывода.

### FLOW_CHART_INTERNAL_STORAGE {#FLOW-CHART-INTERNAL-STORAGE}
```
public static int FLOW_CHART_INTERNAL_STORAGE
```


Поток внутреннего хранилища.

### FLOW_CHART_MAGNETIC_DISK {#FLOW-CHART-MAGNETIC-DISK}
```
public static int FLOW_CHART_MAGNETIC_DISK
```


Поток магнитного диска.

### FLOW_CHART_MAGNETIC_DRUM {#FLOW-CHART-MAGNETIC-DRUM}
```
public static int FLOW_CHART_MAGNETIC_DRUM
```


Поток магнитного барабана.

### FLOW_CHART_MAGNETIC_TAPE {#FLOW-CHART-MAGNETIC-TAPE}
```
public static int FLOW_CHART_MAGNETIC_TAPE
```


Поток магнитной ленты.

### FLOW_CHART_MANUAL_INPUT {#FLOW-CHART-MANUAL-INPUT}
```
public static int FLOW_CHART_MANUAL_INPUT
```


Поток ручного ввода.

### FLOW_CHART_MANUAL_OPERATION {#FLOW-CHART-MANUAL-OPERATION}
```
public static int FLOW_CHART_MANUAL_OPERATION
```


Поток ручной операции.

### FLOW_CHART_MERGE {#FLOW-CHART-MERGE}
```
public static int FLOW_CHART_MERGE
```


Поток слияния.

### FLOW_CHART_MULTIDOCUMENT {#FLOW-CHART-MULTIDOCUMENT}
```
public static int FLOW_CHART_MULTIDOCUMENT
```


Поток многодокументный.

### FLOW_CHART_OFFLINE_STORAGE {#FLOW-CHART-OFFLINE-STORAGE}
```
public static int FLOW_CHART_OFFLINE_STORAGE
```


Поток офлайн-хранилища.

### FLOW_CHART_OFFPAGE_CONNECTOR {#FLOW-CHART-OFFPAGE-CONNECTOR}
```
public static int FLOW_CHART_OFFPAGE_CONNECTOR
```


Поток соединителя вне страницы.

### FLOW_CHART_ONLINE_STORAGE {#FLOW-CHART-ONLINE-STORAGE}
```
public static int FLOW_CHART_ONLINE_STORAGE
```


Поток онлайн-хранилища.

### FLOW_CHART_OR {#FLOW-CHART-OR}
```
public static int FLOW_CHART_OR
```


Поток ИЛИ.

### FLOW_CHART_PREDEFINED_PROCESS {#FLOW-CHART-PREDEFINED-PROCESS}
```
public static int FLOW_CHART_PREDEFINED_PROCESS
```


Поток предопределённого процесса.

### FLOW_CHART_PREPARATION {#FLOW-CHART-PREPARATION}
```
public static int FLOW_CHART_PREPARATION
```


Поток подготовки.

### FLOW_CHART_PROCESS {#FLOW-CHART-PROCESS}
```
public static int FLOW_CHART_PROCESS
```


Поток процесса.

### FLOW_CHART_PUNCHED_CARD {#FLOW-CHART-PUNCHED-CARD}
```
public static int FLOW_CHART_PUNCHED_CARD
```


Поток перфокарты.

### FLOW_CHART_PUNCHED_TAPE {#FLOW-CHART-PUNCHED-TAPE}
```
public static int FLOW_CHART_PUNCHED_TAPE
```


Поток перфорированной ленты.

### FLOW_CHART_SORT {#FLOW-CHART-SORT}
```
public static int FLOW_CHART_SORT
```


Поток сортировки.

### FLOW_CHART_SUMMING_JUNCTION {#FLOW-CHART-SUMMING-JUNCTION}
```
public static int FLOW_CHART_SUMMING_JUNCTION
```


Поток суммирующего узла.

### FLOW_CHART_TERMINATOR {#FLOW-CHART-TERMINATOR}
```
public static int FLOW_CHART_TERMINATOR
```


Поток терминатора.

### FOLDED_CORNER {#FOLDED-CORNER}
```
public static int FOLDED_CORNER
```


Сложенный угол.

### FRAME {#FRAME}
```
public static int FRAME
```


Рамка.

### FUNNEL {#FUNNEL}
```
public static int FUNNEL
```


Воронка.

### GEAR_6 {#GEAR-6}
```
public static int GEAR_6
```


Шестерня с шестью зубьями.

### GEAR_9 {#GEAR-9}
```
public static int GEAR_9
```


Шестерня с девятью зубьями.

### HALF_FRAME {#HALF-FRAME}
```
public static int HALF_FRAME
```


Полурама.

### HEART {#HEART}
```
public static int HEART
```


Сердце.

### HEPTAGON {#HEPTAGON}
```
public static int HEPTAGON
```


Семигранник.

### HEXAGON {#HEXAGON}
```
public static int HEXAGON
```


Шестиугольник.

### HOME_PLATE {#HOME-PLATE}
```
public static int HOME_PLATE
```


Домашняя плита.

### HORIZONTAL_SCROLL {#HORIZONTAL-SCROLL}
```
public static int HORIZONTAL_SCROLL
```


Горизонтальная прокрутка.

### INVERSE_LINE {#INVERSE-LINE}
```
public static int INVERSE_LINE
```


Обратная линия.

### IRREGULAR_SEAL_1 {#IRREGULAR-SEAL-1}
```
public static int IRREGULAR_SEAL_1
```


Нерегулярное уплотнение 1.

### IRREGULAR_SEAL_2 {#IRREGULAR-SEAL-2}
```
public static int IRREGULAR_SEAL_2
```


Нерегулярное уплотнение 2.

### LEFT_ARROW {#LEFT-ARROW}
```
public static int LEFT_ARROW
```


Стрелка влево.

### LEFT_ARROW_CALLOUT {#LEFT-ARROW-CALLOUT}
```
public static int LEFT_ARROW_CALLOUT
```


Выноска со стрелкой влево.

### LEFT_BRACE {#LEFT-BRACE}
```
public static int LEFT_BRACE
```


Левая фигурная скобка.

### LEFT_BRACKET {#LEFT-BRACKET}
```
public static int LEFT_BRACKET
```


Левая квадратная скобка.

### LEFT_CIRCULAR_ARROW {#LEFT-CIRCULAR-ARROW}
```
public static int LEFT_CIRCULAR_ARROW
```


Левая круговая стрелка.

### LEFT_RIGHT_ARROW {#LEFT-RIGHT-ARROW}
```
public static int LEFT_RIGHT_ARROW
```


Стрелка влево и вправо.

### LEFT_RIGHT_ARROW_CALLOUT {#LEFT-RIGHT-ARROW-CALLOUT}
```
public static int LEFT_RIGHT_ARROW_CALLOUT
```


Выноска со стрелкой влево и вправо.

### LEFT_RIGHT_CIRCULAR_ARROW {#LEFT-RIGHT-CIRCULAR-ARROW}
```
public static int LEFT_RIGHT_CIRCULAR_ARROW
```


Круговая стрелка слева направо.

### LEFT_RIGHT_RIBBON {#LEFT-RIGHT-RIBBON}
```
public static int LEFT_RIGHT_RIBBON
```


Лента слева направо.

### LEFT_RIGHT_UP_ARROW {#LEFT-RIGHT-UP-ARROW}
```
public static int LEFT_RIGHT_UP_ARROW
```


Стрелка влево‑вправо‑вверх.

### LEFT_UP_ARROW {#LEFT-UP-ARROW}
```
public static int LEFT_UP_ARROW
```


Стрелка влево‑вверх.

### LIGHTNING_BOLT {#LIGHTNING-BOLT}
```
public static int LIGHTNING_BOLT
```


Молния.

### LINE {#LINE}
```
public static int LINE
```


Линия.

### MATH_DIVIDE {#MATH-DIVIDE}
```
public static int MATH_DIVIDE
```


Знак деления.

### MATH_EQUAL {#MATH-EQUAL}
```
public static int MATH_EQUAL
```


Знак равенства.

### MATH_MINUS {#MATH-MINUS}
```
public static int MATH_MINUS
```


Знак вычитания.

### MATH_MULTIPLY {#MATH-MULTIPLY}
```
public static int MATH_MULTIPLY
```


Знак умножения.

### MATH_NOT_EQUAL {#MATH-NOT-EQUAL}
```
public static int MATH_NOT_EQUAL
```


Знак неравенства.

### MATH_PLUS {#MATH-PLUS}
```
public static int MATH_PLUS
```


Знак сложения.

### MOON {#MOON}
```
public static int MOON
```


Луна.

### NON_ISOSCELES_TRAPEZOID {#NON-ISOSCELES-TRAPEZOID}
```
public static int NON_ISOSCELES_TRAPEZOID
```


Неравнобедренная трапеция.

### NOTCHED_RIGHT_ARROW {#NOTCHED-RIGHT-ARROW}
```
public static int NOTCHED_RIGHT_ARROW
```


Стрелка вправо с вырезом.

### NO_SMOKING {#NO-SMOKING}
```
public static int NO_SMOKING
```


Запрет курения.

### OCTAGON {#OCTAGON}
```
public static int OCTAGON
```


Восьмиугольник.

### PARALLELOGRAM {#PARALLELOGRAM}
```
public static int PARALLELOGRAM
```


Параллелограмм.

### PENTAGON {#PENTAGON}
```
public static int PENTAGON
```


Пятиугольник.

### PIE {#PIE}
```
public static int PIE
```


Круговая диаграмма.

### PLAQUE {#PLAQUE}
```
public static int PLAQUE
```


Табличка.

### PLAQUE_TABS {#PLAQUE-TABS}
```
public static int PLAQUE_TABS
```


Вкладки таблички.

### PLUS {#PLUS}
```
public static int PLUS
```


Плюс.

### QUAD_ARROW {#QUAD-ARROW}
```
public static int QUAD_ARROW
```


Стрелка в четыре стороны.

### QUAD_ARROW_CALLOUT {#QUAD-ARROW-CALLOUT}
```
public static int QUAD_ARROW_CALLOUT
```


Выноска с четырёхстрелкой.

### RECTANGLE {#RECTANGLE}
```
public static int RECTANGLE
```


Прямоугольник.

### RIBBON {#RIBBON}
```
public static int RIBBON
```


Лента.

### RIBBON_2 {#RIBBON-2}
```
public static int RIBBON_2
```


Лента 2.

### RIGHT_ARROW_CALLOUT {#RIGHT-ARROW-CALLOUT}
```
public static int RIGHT_ARROW_CALLOUT
```


Врезка со стрелкой вправо.

### RIGHT_BRACE {#RIGHT-BRACE}
```
public static int RIGHT_BRACE
```


Правая фигурная скобка.

### RIGHT_BRACKET {#RIGHT-BRACKET}
```
public static int RIGHT_BRACKET
```


Правая квадратная скобка.

### RIGHT_TRIANGLE {#RIGHT-TRIANGLE}
```
public static int RIGHT_TRIANGLE
```


Правый треугольник.

### ROUND_RECTANGLE {#ROUND-RECTANGLE}
```
public static int ROUND_RECTANGLE
```


Скруглённый прямоугольник.

### SEAL_10 {#SEAL-10}
```
public static int SEAL_10
```


Звезда с десятью лучами.

### SEAL_12 {#SEAL-12}
```
public static int SEAL_12
```


Звезда с двенадцатью лучами.

### SEAL_16 {#SEAL-16}
```
public static int SEAL_16
```


Звезда с шестнадцатью лучами.

### SEAL_24 {#SEAL-24}
```
public static int SEAL_24
```


Звезда с двадцатью четырьмя лучами.

### SEAL_32 {#SEAL-32}
```
public static int SEAL_32
```


Звезда с тридцатью двумя лучами.

### SEAL_4 {#SEAL-4}
```
public static int SEAL_4
```


Звезда с четырьмя лучами.

### SEAL_6 {#SEAL-6}
```
public static int SEAL_6
```


Звезда с шестью лучами.

### SEAL_7 {#SEAL-7}
```
public static int SEAL_7
```


Звезда с семью лучами.

### SEAL_8 {#SEAL-8}
```
public static int SEAL_8
```


Звезда с восемью лучами.

### SINGLE_CORNER_ROUNDED {#SINGLE-CORNER-ROUNDED}
```
public static int SINGLE_CORNER_ROUNDED
```


Скруглённый прямоугольник с одной скруглённой стороной.

### SINGLE_CORNER_SNIPPED {#SINGLE-CORNER-SNIPPED}
```
public static int SINGLE_CORNER_SNIPPED
```


Объект с вырезанным углом у прямоугольника.

### SMILEY_FACE {#SMILEY-FACE}
```
public static int SMILEY_FACE
```


Смайлик.

### SQUARE_TABS {#SQUARE-TABS}
```
public static int SQUARE_TABS
```


Квадратные вкладки.

### STAR {#STAR}
```
public static int STAR
```


Звезда.

### STRAIGHT_CONNECTOR_1 {#STRAIGHT-CONNECTOR-1}
```
public static int STRAIGHT_CONNECTOR_1
```


Прямой соединитель 1.

### STRIPED_RIGHT_ARROW {#STRIPED-RIGHT-ARROW}
```
public static int STRIPED_RIGHT_ARROW
```


Полосатая стрелка вправо.

### SUN {#SUN}
```
public static int SUN
```


Солнце.

### SWOOSH_ARROW {#SWOOSH-ARROW}
```
public static int SWOOSH_ARROW
```


Стрелка‑свисток.

### TEARDROP {#TEARDROP}
```
public static int TEARDROP
```


Капля.

### TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED {#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED}
```
public static int TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED
```


Прямоугольник с отрезанным и скруглённым одним углом.

### TOP_CORNERS_ROUNDED {#TOP-CORNERS-ROUNDED}
```
public static int TOP_CORNERS_ROUNDED
```


Прямоугольник с округлым углом одной стороны.

### TOP_CORNERS_SNIPPED {#TOP-CORNERS-SNIPPED}
```
public static int TOP_CORNERS_SNIPPED
```


Прямоугольник с отрезанным углом одной стороны.

### TRAPEZOID {#TRAPEZOID}
```
public static int TRAPEZOID
```


Трапеция.

### TRIANGLE {#TRIANGLE}
```
public static int TRIANGLE
```


Треугольник.

### UP_ARROW {#UP-ARROW}
```
public static int UP_ARROW
```


Стрелка вверх.

### UP_ARROW_CALLOUT {#UP-ARROW-CALLOUT}
```
public static int UP_ARROW_CALLOUT
```


Выноска со стрелкой вверх.

### UP_DOWN_ARROW {#UP-DOWN-ARROW}
```
public static int UP_DOWN_ARROW
```


Стрелка вверх и вниз.

### UP_DOWN_ARROW_CALLOUT {#UP-DOWN-ARROW-CALLOUT}
```
public static int UP_DOWN_ARROW_CALLOUT
```


Выноска со стрелкой вверх и вниз.

### UTURN_ARROW {#UTURN-ARROW}
```
public static int UTURN_ARROW
```


Стрелка разворота.

### VERTICAL_SCROLL {#VERTICAL-SCROLL}
```
public static int VERTICAL_SCROLL
```


Вертикальная прокрутка.

### WAVE {#WAVE}
```
public static int WAVE
```


Волна.

### WEDGE_ELLIPSE_CALLOUT {#WEDGE-ELLIPSE-CALLOUT}
```
public static int WEDGE_ELLIPSE_CALLOUT
```


Выноска с сектором эллипса.

### WEDGE_PIE {#WEDGE-PIE}
```
public static int WEDGE_PIE
```


Секторный круг.

### WEDGE_RECT_CALLOUT {#WEDGE-RECT-CALLOUT}
```
public static int WEDGE_RECT_CALLOUT
```


Выноска с сектором прямоугольника.

### WEDGE_R_RECT_CALLOUT {#WEDGE-R-RECT-CALLOUT}
```
public static int WEDGE_R_RECT_CALLOUT
```


Выноска с сектором скруглённого прямоугольника.

### length {#length}
```
public static int length
```


### fromName(String chartShapeTypeName) {#fromName-java.lang.String}
```
public static int fromName(String chartShapeTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| chartShapeTypeName | java.lang.String |  |

**Returns:**
int
### getName(int chartShapeType) {#getName-int}
```
public static String getName(int chartShapeType)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| chartShapeType | int |  |

**Returns:**
java.lang.String
