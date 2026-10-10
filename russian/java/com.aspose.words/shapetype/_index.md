---
title: "ShapeType"
linktitle: "ShapeType"
second_title: "Aspose.Words для Java"
description: "Указывает тип фигуры в документе Microsoft Word на Java."
type: docs
weight: 618
url: /ru/java/com.aspose.words/shapetype/
---

**Inheritance:**
java.lang.Object
```
public class ShapeType
```

Указывает тип фигуры в документе Microsoft Word.

 **Examples:** 

Показывает, как вставить фигуру с изображением из локальной файловой системы в документ.

```

 Document doc = new Document();

 // The "Shape" class's public constructor will create a shape with "ShapeMarkupLanguage.Vml" markup type.
 // If you need to create a shape of a non-primitive type, such as SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
 // TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, or DiagonalCornersRounded,
 // please use DocumentBuilder.InsertShape.
 Shape shape = new Shape(doc, ShapeType.IMAGE);
 shape.getImageData().setImage(getImageDir() + "Windows MetaFile.wmf");
 shape.setWidth(100.0);
 shape.setHeight(100.0);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(shape);

 doc.save(getArtifactsDir() + "Image.FromFile.docx");
 
```

Показывает, как Aspose.Words определяет фигуры.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertShape(ShapeType.HEPTAGON, RelativeHorizontalPosition.PAGE, 0.0,
         RelativeVerticalPosition.PAGE, 0.0, 0.0, 0.0, WrapType.NONE);

 builder.insertShape(ShapeType.CLOUD, RelativeHorizontalPosition.RIGHT_MARGIN, 0.0,
         RelativeVerticalPosition.PAGE, 0.0, 0.0, 0.0, WrapType.NONE);

 builder.insertShape(ShapeType.MATH_PLUS, RelativeHorizontalPosition.RIGHT_MARGIN, 0.0,
         RelativeVerticalPosition.PAGE, 0.0, 0.0, 0.0, WrapType.NONE);

 // To correct identify shape types you need to work with shapes as DML.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.DOCX);
 {
     // "Strict" or "Transitional" compliance allows to save shape as DML.
     saveOptions.setCompliance(OoxmlCompliance.ISO_29500_2008_TRANSITIONAL);
 }

 doc.save(getArtifactsDir() + "Shape.ShapeTypes.docx", saveOptions);
 doc = new Document(getArtifactsDir() + "Shape.ShapeTypes.docx");

 List shapes = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 for (Shape shape : shapes)
 {
     System.out.println(shape.getShapeType());
 }
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [ACCENT_BORDER_CALLOUT_1](#ACCENT-BORDER-CALLOUT-1) | Вызов границы акцента 1. |
| [ACCENT_BORDER_CALLOUT_2](#ACCENT-BORDER-CALLOUT-2) | Вызов границы акцента 2. |
| [ACCENT_BORDER_CALLOUT_3](#ACCENT-BORDER-CALLOUT-3) | Вызов границы акцента 3. |
| [ACCENT_BORDER_CALLOUT_90](#ACCENT-BORDER-CALLOUT-90) | Вызов границы акцента 90. |
| [ACCENT_CALLOUT_1](#ACCENT-CALLOUT-1) | Фигура вызова акцента с одной стрелкой. |
| [ACCENT_CALLOUT_2](#ACCENT-CALLOUT-2) | Фигура вызова акцента с двумя стрелками. |
| [ACCENT_CALLOUT_3](#ACCENT-CALLOUT-3) | Фигура вызова акцента с тремя стрелками. |
| [ACCENT_CALLOUT_90](#ACCENT-CALLOUT-90) | Вызов акцента 90. |
| [ACTION_BUTTON_BACK_PREVIOUS](#ACTION-BUTTON-BACK-PREVIOUS) | Кнопка действия назад предыдущий. |
| [ACTION_BUTTON_BEGINNING](#ACTION-BUTTON-BEGINNING) | Кнопка действия начало. |
| [ACTION_BUTTON_BLANK](#ACTION-BUTTON-BLANK) | Кнопка действия пустой. |
| [ACTION_BUTTON_DOCUMENT](#ACTION-BUTTON-DOCUMENT) | Кнопка действия документ. |
| [ACTION_BUTTON_END](#ACTION-BUTTON-END) | Кнопка действия конец. |
| [ACTION_BUTTON_FORWARD_NEXT](#ACTION-BUTTON-FORWARD-NEXT) | Кнопка действия вперёд следующий. |
| [ACTION_BUTTON_HELP](#ACTION-BUTTON-HELP) | Кнопка действия справка. |
| [ACTION_BUTTON_HOME](#ACTION-BUTTON-HOME) | Кнопка действия домой. |
| [ACTION_BUTTON_INFORMATION](#ACTION-BUTTON-INFORMATION) | Кнопка действия информация. |
| [ACTION_BUTTON_MOVIE](#ACTION-BUTTON-MOVIE) | Кнопка действия фильм. |
| [ACTION_BUTTON_RETURN](#ACTION-BUTTON-RETURN) | Кнопка действия возврат. |
| [ACTION_BUTTON_SOUND](#ACTION-BUTTON-SOUND) | Кнопка действия звук. |
| [ARC](#ARC) | Дуга. |
| [ARROW](#ARROW) | Стрелка. |
| [BALLOON](#BALLOON) | Шар. |
| [BENT_ARROW](#BENT-ARROW) | Согнутая стрелка. |
| [BENT_CONNECTOR_2](#BENT-CONNECTOR-2) | Изогнутая соединительная фигура с двумя сегментами. |
| [BENT_CONNECTOR_3](#BENT-CONNECTOR-3) | Изогнутая соединительная фигура с тремя сегментами. |
| [BENT_CONNECTOR_4](#BENT-CONNECTOR-4) | Изогнутая соединительная фигура с четырьмя сегментами. |
| [BENT_CONNECTOR_5](#BENT-CONNECTOR-5) | Изогнутая соединительная фигура с пятью сегментами. |
| [BENT_UP_ARROW](#BENT-UP-ARROW) | Согнутая стрелка вверх. |
| [BEVEL](#BEVEL) | Скос. |
| [BLOCK_ARC](#BLOCK-ARC) | Блочная дуга. |
| [BORDER_CALLOUT_1](#BORDER-CALLOUT-1) | Выноска границы 1. |
| [BORDER_CALLOUT_2](#BORDER-CALLOUT-2) | Выноска границы 2. |
| [BORDER_CALLOUT_3](#BORDER-CALLOUT-3) | Выноска границы 3. |
| [BORDER_CALLOUT_90](#BORDER-CALLOUT-90) | Выноска границы 90. |
| [BRACE_PAIR](#BRACE-PAIR) | Пара скобок |
| [BRACKET_PAIR](#BRACKET-PAIR) | Парные квадратные скобки. |
| [CALLOUT_1](#CALLOUT-1) | Фигура выноски с одной стрелкой. |
| [CALLOUT_2](#CALLOUT-2) | Фигура выноски с двумя стрелками. |
| [CALLOUT_3](#CALLOUT-3) | Фигура выноски с тремя стрелками. |
| [CALLOUT_90](#CALLOUT-90) | Выноска 90. |
| [CAN](#CAN) | Банка. |
| [CHART_PLUS](#CHART-PLUS) | Диаграмма плюс. |
| [CHART_STAR](#CHART-STAR) | Диаграмма звезда. |
| [CHART_X](#CHART-X) | Диаграмма X. |
| [CHEVRON](#CHEVRON) | Шеврон. |
| [CHORD](#CHORD) | Хорда. |
| [CIRCULAR_ARROW](#CIRCULAR-ARROW) | Круговая стрелка. |
| [CLOUD](#CLOUD) | Облако. |
| [CLOUD_CALLOUT](#CLOUD-CALLOUT) | Облачная выноска. |
| [CORNER](#CORNER) | Угол. |
| [CORNER_TABS](#CORNER-TABS) | Угловые вкладки. |
| [CUBE](#CUBE) | Куб. |
| [CURVED_CONNECTOR_2](#CURVED-CONNECTOR-2) | Изогнутая соединительная фигура с двумя сегментами. |
| [CURVED_CONNECTOR_3](#CURVED-CONNECTOR-3) | Изогнутая соединительная фигура с тремя сегментами. |
| [CURVED_CONNECTOR_4](#CURVED-CONNECTOR-4) | Изогнутая соединительная фигура с четырьмя сегментами. |
| [CURVED_CONNECTOR_5](#CURVED-CONNECTOR-5) | Изогнутая соединительная фигура с пятью сегментами. |
| [CURVED_DOWN_ARROW](#CURVED-DOWN-ARROW) | Изогнутая стрелка вниз. |
| [CURVED_LEFT_ARROW](#CURVED-LEFT-ARROW) | Изогнутая стрелка влево. |
| [CURVED_RIGHT_ARROW](#CURVED-RIGHT-ARROW) | Изогнутая стрелка вправо. |
| [CURVED_UP_ARROW](#CURVED-UP-ARROW) | Изогнутая стрелка вверх. |
| [CUSTOM_SHAPE](#CUSTOM-SHAPE) | Похоже, что этот тип фигуры предназначен для фигур, которые не входят в стандартный набор автофигур в Microsoft Word. |
| [DECAGON](#DECAGON) | Десятиугольник. |
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
| [FLOW_CHART_ALTERNATE_PROCESS](#FLOW-CHART-ALTERNATE-PROCESS) | Блок-схема: альтернативный процесс. |
| [FLOW_CHART_COLLATE](#FLOW-CHART-COLLATE) | Блок-схема: собрать. |
| [FLOW_CHART_CONNECTOR](#FLOW-CHART-CONNECTOR) | Блок-схема: соединитель. |
| [FLOW_CHART_DECISION](#FLOW-CHART-DECISION) | Блок-схема: решение. |
| [FLOW_CHART_DELAY](#FLOW-CHART-DELAY) | Блок-схема: задержка. |
| [FLOW_CHART_DISPLAY](#FLOW-CHART-DISPLAY) | Блок-схема: отображение. |
| [FLOW_CHART_DOCUMENT](#FLOW-CHART-DOCUMENT) | Блок-схема: документ. |
| [FLOW_CHART_EXTRACT](#FLOW-CHART-EXTRACT) | Блок-схема: извлечение. |
| [FLOW_CHART_INPUT_OUTPUT](#FLOW-CHART-INPUT-OUTPUT) | Блок-схема: ввод‑вывод. |
| [FLOW_CHART_INTERNAL_STORAGE](#FLOW-CHART-INTERNAL-STORAGE) | Блок-схема: внутреннее хранилище. |
| [FLOW_CHART_MAGNETIC_DISK](#FLOW-CHART-MAGNETIC-DISK) | Блок-схема: магнитный диск. |
| [FLOW_CHART_MAGNETIC_DRUM](#FLOW-CHART-MAGNETIC-DRUM) | Блок-схема: магнитный барабан. |
| [FLOW_CHART_MAGNETIC_TAPE](#FLOW-CHART-MAGNETIC-TAPE) | Блок-схема char магнитная лента. |
| [FLOW_CHART_MANUAL_INPUT](#FLOW-CHART-MANUAL-INPUT) | Блок-схема: ручной ввод. |
| [FLOW_CHART_MANUAL_OPERATION](#FLOW-CHART-MANUAL-OPERATION) | Блок-схема: ручная операция. |
| [FLOW_CHART_MERGE](#FLOW-CHART-MERGE) | Блок-схема: объединение. |
| [FLOW_CHART_MULTIDOCUMENT](#FLOW-CHART-MULTIDOCUMENT) | Блок-схема: многодокументный. |
| [FLOW_CHART_OFFLINE_STORAGE](#FLOW-CHART-OFFLINE-STORAGE) | Блок-схема: офлайн‑хранилище. |
| [FLOW_CHART_OFFPAGE_CONNECTOR](#FLOW-CHART-OFFPAGE-CONNECTOR) | Блок-схема: соединитель за пределами страницы. |
| [FLOW_CHART_ONLINE_STORAGE](#FLOW-CHART-ONLINE-STORAGE) | Блок-схема: онлайн‑хранилище. |
| [FLOW_CHART_OR](#FLOW-CHART-OR) | Блок-схема или. |
| [FLOW_CHART_PREDEFINED_PROCESS](#FLOW-CHART-PREDEFINED-PROCESS) | Предопределенный процесс блок-схемы |
| [FLOW_CHART_PREPARATION](#FLOW-CHART-PREPARATION) | Подготовка блок-схемы. |
| [FLOW_CHART_PROCESS](#FLOW-CHART-PROCESS) | Процесс блок-схемы. |
| [FLOW_CHART_PUNCHED_CARD](#FLOW-CHART-PUNCHED-CARD) | Перфокарта блок-схемы. |
| [FLOW_CHART_PUNCHED_TAPE](#FLOW-CHART-PUNCHED-TAPE) | Перфолента блок-схемы. |
| [FLOW_CHART_SORT](#FLOW-CHART-SORT) | Сортировка блок-схемы. |
| [FLOW_CHART_SUMMING_JUNCTION](#FLOW-CHART-SUMMING-JUNCTION) | Суммирующий узел блок-схемы. |
| [FLOW_CHART_TERMINATOR](#FLOW-CHART-TERMINATOR) | Терминатор блок-схемы. |
| [FOLDED_CORNER](#FOLDED-CORNER) | Сложенный угол. |
| [FRAME](#FRAME) | Рамка. |
| [FUNNEL](#FUNNEL) | Воронка. |
| [GEAR_6](#GEAR-6) | Шестерня с шестью зубьями. |
| [GEAR_9](#GEAR-9) | Шестерня с девятью зубьями. |
| [GROUP](#GROUP) | Фигура является групповой фигурой. |
| [HALF_FRAME](#HALF-FRAME) | Полурама. |
| [HEART](#HEART) | Сердце. |
| [HEPTAGON](#HEPTAGON) | Семигранник. |
| [HEXAGON](#HEXAGON) | Шестиугольник. |
| [HOME_PLATE](#HOME-PLATE) | Домашняя плита. |
| [HORIZONTAL_SCROLL](#HORIZONTAL-SCROLL) | Горизонтальная прокрутка. |
| [IMAGE](#IMAGE) | Фигура является изображением. |
| [INVERSE_LINE](#INVERSE-LINE) | Обратная линия. |
| [IRREGULAR_SEAL_1](#IRREGULAR-SEAL-1) | Нерегулярное уплотнение 1. |
| [IRREGULAR_SEAL_2](#IRREGULAR-SEAL-2) | Нерегулярное уплотнение 2. |
| [LEFT_ARROW](#LEFT-ARROW) | Стрелка влево. |
| [LEFT_ARROW_CALLOUT](#LEFT-ARROW-CALLOUT) | Выноска со стрелкой влево. |
| [LEFT_BRACE](#LEFT-BRACE) | Левая фигурная скобка. |
| [LEFT_BRACKET](#LEFT-BRACKET) | Левая квадратная скобка. |
| [LEFT_CIRCULAR_ARROW](#LEFT-CIRCULAR-ARROW) | Левая круговая стрелка. |
| [LEFT_RIGHT_ARROW](#LEFT-RIGHT-ARROW) | Стрелка влево‑вправо. |
| [LEFT_RIGHT_ARROW_CALLOUT](#LEFT-RIGHT-ARROW-CALLOUT) | Выноска со стрелкой влево‑вправо. |
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
| [MIN_VALUE](#MIN-VALUE) | Зарезервировано для использования системой. |
| [MOON](#MOON) | Луна. |
| [NON_ISOSCELES_TRAPEZOID](#NON-ISOSCELES-TRAPEZOID) | Неравнобедренная трапеция. |
| [NON_PRIMITIVE](#NON-PRIMITIVE) | Фигура, нарисованная пользователем и состоящая из нескольких сегментов и/или вершин (кривая, произвольная форма или каракули). |
| [NOTCHED_RIGHT_ARROW](#NOTCHED-RIGHT-ARROW) | Стрелка вправо с вырезом. |
| [NO_SMOKING](#NO-SMOKING) | NoSmoking. |
| [OCTAGON](#OCTAGON) | Восьмиугольник. |
| [OLE_CONTROL](#OLE-CONTROL) | Фигура является элементом управления ActiveX. |
| [OLE_OBJECT](#OLE-OBJECT) | Фигура является объектом OLE. |
| [PARALLELOGRAM](#PARALLELOGRAM) | Параллелограмм. |
| [PENTAGON](#PENTAGON) | Пятиугольник. |
| [PIE](#PIE) | Круговая диаграмма. |
| [PLAQUE](#PLAQUE) | Табличка. |
| [PLAQUE_TABS](#PLAQUE-TABS) | Вкладки таблички. |
| [PLUS](#PLUS) | Плюс. |
| [QUAD_ARROW](#QUAD-ARROW) | Стрелка в четыре стороны. |
| [QUAD_ARROW_CALLOUT](#QUAD-ARROW-CALLOUT) | Выноска с четырёхстрелочной стрелкой. |
| [RECTANGLE](#RECTANGLE) | Прямоугольник. |
| [RIBBON](#RIBBON) | Лента. |
| [RIBBON_2](#RIBBON-2) | Лента 2. |
| [RIGHT_ARROW_CALLOUT](#RIGHT-ARROW-CALLOUT) | Выноска со стрелкой вправо |
| [RIGHT_BRACE](#RIGHT-BRACE) | Правая фигурная скобка. |
| [RIGHT_BRACKET](#RIGHT-BRACKET) | Правая квадратная скобка. |
| [RIGHT_TRIANGLE](#RIGHT-TRIANGLE) | Правый треугольник. |
| [ROUND_RECTANGLE](#ROUND-RECTANGLE) | Закруглённый прямоугольник. |
| [SEAL](#SEAL) | Печать. |
| [SEAL_10](#SEAL-10) | Звезда с десятью лучами. |
| [SEAL_12](#SEAL-12) | Звезда с двенадцатью лучами. |
| [SEAL_16](#SEAL-16) | Звезда с шестнадцатью лучами. |
| [SEAL_24](#SEAL-24) | Звезда с 24 лучами. |
| [SEAL_32](#SEAL-32) | Звезда с 32 лучами. |
| [SEAL_4](#SEAL-4) | Звезда с четырьмя лучами. |
| [SEAL_6](#SEAL-6) | Звезда с шестью лучами. |
| [SEAL_7](#SEAL-7) | Звезда с семью лучами. |
| [SEAL_8](#SEAL-8) | Звезда с восемью лучами. |
| [SINGLE_CORNER_ROUNDED](#SINGLE-CORNER-ROUNDED) | Прямоугольник с одной скруглённой стороной. |
| [SINGLE_CORNER_SNIPPED](#SINGLE-CORNER-SNIPPED) | Объект с вырезанным углом у прямоугольника. |
| [SMILEY_FACE](#SMILEY-FACE) | Смайлик. |
| [SQUARE_TABS](#SQUARE-TABS) | Квадратные вкладки. |
| [STAR](#STAR) | Звезда. |
| [STRAIGHT_CONNECTOR_1](#STRAIGHT-CONNECTOR-1) | Прямая соединительная фигура. |
| [STRIPED_RIGHT_ARROW](#STRIPED-RIGHT-ARROW) | Полосатая стрелка вправо. |
| [SUN](#SUN) | Солнце. |
| [SWOOSH_ARROW](#SWOOSH-ARROW) | Стрелка‑свисток. |
| [TEARDROP](#TEARDROP) | Капля. |
| [TEXT_ARCH_DOWN_CURVE](#TEXT-ARCH-DOWN-CURVE) | Арка вниз, объект WordArt. |
| [TEXT_ARCH_DOWN_POUR](#TEXT-ARCH-DOWN-POUR) | Арка вниз, заливка, объект WordArt. |
| [TEXT_ARCH_UP_CURVE](#TEXT-ARCH-UP-CURVE) | Арка вверх, объект WordArt. |
| [TEXT_ARCH_UP_POUR](#TEXT-ARCH-UP-POUR) | Арка вверх, заливка, объект WordArt. |
| [TEXT_BOX](#TEXT-BOX) | Эта фигура — текстовое поле. |
| [TEXT_BUTTON_CURVE](#TEXT-BUTTON-CURVE) | Кнопка кривая, объект WordArt. |
| [TEXT_BUTTON_POUR](#TEXT-BUTTON-POUR) | Кнопка заливка, объект WordArt. |
| [TEXT_CAN_DOWN](#TEXT-CAN-DOWN) | Банка вниз, объект WordArt. |
| [TEXT_CAN_UP](#TEXT-CAN-UP) | Банка вверх, объект WordArt. |
| [TEXT_CASCADE_DOWN](#TEXT-CASCADE-DOWN) | Каскад вниз, объект WordArt. |
| [TEXT_CASCADE_UP](#TEXT-CASCADE-UP) | Каскад вверх, объект WordArt. |
| [TEXT_CHEVRON](#TEXT-CHEVRON) | Шеврон, объект WordArt. |
| [TEXT_CHEVRON_INVERTED](#TEXT-CHEVRON-INVERTED) | Шеврон перевёрнутый, объект WordArt. |
| [TEXT_CIRCLE_CURVE](#TEXT-CIRCLE-CURVE) | Круг кривая, объект WordArt. |
| [TEXT_CIRCLE_POUR](#TEXT-CIRCLE-POUR) | Круг заливка, объект WordArt. |
| [TEXT_CURVE](#TEXT-CURVE) | Текстовая кривая. |
| [TEXT_CURVE_DOWN](#TEXT-CURVE-DOWN) | Кривая вниз, объект WordArt. |
| [TEXT_CURVE_UP](#TEXT-CURVE-UP) | Кривая вверх, объект WordArt. |
| [TEXT_DEFLATE](#TEXT-DEFLATE) | Сжать, объект WordArt. |
| [TEXT_DEFLATE_BOTTOM](#TEXT-DEFLATE-BOTTOM) | Сжать снизу, объект WordArt. |
| [TEXT_DEFLATE_INFLATE](#TEXT-DEFLATE-INFLATE) | Сжать развернуть, объект WordArt. |
| [TEXT_DEFLATE_INFLATE_DEFLATE](#TEXT-DEFLATE-INFLATE-DEFLATE) | Сжать развернуть сжать, объект WordArt. |
| [TEXT_DEFLATE_TOP](#TEXT-DEFLATE-TOP) | Сжать сверху, объект WordArt. |
| [TEXT_FADE_DOWN](#TEXT-FADE-DOWN) | Исчезать вниз, объект WordArt. |
| [TEXT_FADE_LEFT](#TEXT-FADE-LEFT) | Исчезать влево, объект WordArt. |
| [TEXT_FADE_RIGHT](#TEXT-FADE-RIGHT) | Исчезать вправо, объект WordArt. |
| [TEXT_FADE_UP](#TEXT-FADE-UP) | Исчезать вверх, объект WordArt. |
| [TEXT_HEXAGON](#TEXT-HEXAGON) | Текст шестиугольник. |
| [TEXT_INFLATE](#TEXT-INFLATE) | Раздуть, объект WordArt. |
| [TEXT_INFLATE_BOTTOM](#TEXT-INFLATE-BOTTOM) | Раздуть снизу, объект WordArt. |
| [TEXT_INFLATE_TOP](#TEXT-INFLATE-TOP) | Раздуть сверху, объект WordArt. |
| [TEXT_OCTAGON](#TEXT-OCTAGON) | Текст восьмиугольник. |
| [TEXT_ON_CURVE](#TEXT-ON-CURVE) | Текст по кривой. |
| [TEXT_ON_RING](#TEXT-ON-RING) | Текст по кольцу. |
| [TEXT_PLAIN_TEXT](#TEXT-PLAIN-TEXT) | Простой текст, объект WordArt. |
| [TEXT_RING](#TEXT-RING) | Текстовое кольцо. |
| [TEXT_RING_INSIDE](#TEXT-RING-INSIDE) | Кольцо внутри, объект WordArt. |
| [TEXT_RING_OUTSIDE](#TEXT-RING-OUTSIDE) | Кольцо снаружи, объект WordArt. |
| [TEXT_SIMPLE](#TEXT-SIMPLE) | Простой текст. |
| [TEXT_SLANT_DOWN](#TEXT-SLANT-DOWN) | Наклон вниз, объект WordArt. |
| [TEXT_SLANT_UP](#TEXT-SLANT-UP) | Наклон вверх, объект WordArt. |
| [TEXT_STOP](#TEXT-STOP) | Стоп, объект WordArt. |
| [TEXT_TRIANGLE](#TEXT-TRIANGLE) | Треугольник, объект WordArt. |
| [TEXT_TRIANGLE_INVERTED](#TEXT-TRIANGLE-INVERTED) | Перевернутый треугольник, объект WordArt. |
| [TEXT_WAVE](#TEXT-WAVE) | Текстовая волна. |
| [TEXT_WAVE_1](#TEXT-WAVE-1) | Волна 1, объект WordArt. |
| [TEXT_WAVE_2](#TEXT-WAVE-2) | Волна 2, объект WordArt. |
| [TEXT_WAVE_3](#TEXT-WAVE-3) | Волна 3, объект WordArt. |
| [TEXT_WAVE_4](#TEXT-WAVE-4) | Волна 4, объект WordArt. |
| [THICK_ARROW](#THICK-ARROW) | Толстая стрелка. |
| [TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED](#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED) | Прямоугольник с отрезанным и скруглённым одним углом. |
| [TOP_CORNERS_ROUNDED](#TOP-CORNERS-ROUNDED) | Прямоугольник с закругленным углом одной стороны. |
| [TOP_CORNERS_SNIPPED](#TOP-CORNERS-SNIPPED) | Прямоугольник с отрезанным углом одной стороны. |
| [TRAPEZOID](#TRAPEZOID) | Трапеция. |
| [TRIANGLE](#TRIANGLE) | Треугольник. |
| [UP_ARROW](#UP-ARROW) | Стрелка вверх. |
| [UP_ARROW_CALLOUT](#UP-ARROW-CALLOUT) | Врезка со стрелкой вверх. |
| [UP_DOWN_ARROW](#UP-DOWN-ARROW) | Стрелка вверх‑вниз. |
| [UP_DOWN_ARROW_CALLOUT](#UP-DOWN-ARROW-CALLOUT) | Врезка со стрелкой вверх‑вниз. |
| [UTURN_ARROW](#UTURN-ARROW) | Стрелка разворота. |
| [VERTICAL_SCROLL](#VERTICAL-SCROLL) | Вертикальная прокрутка. |
| [WAVE](#WAVE) | Волна. |
| [WEDGE_ELLIPSE_CALLOUT](#WEDGE-ELLIPSE-CALLOUT) | Врезка в виде клина эллипса. |
| [WEDGE_PIE](#WEDGE-PIE) | Секторный круг. |
| [WEDGE_RECT_CALLOUT](#WEDGE-RECT-CALLOUT) | Врезка в виде клина прямоугольника. |
| [WEDGE_R_RECT_CALLOUT](#WEDGE-R-RECT-CALLOUT) | Врезка в виде клина R‑прямоугольника. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String shapeTypeName)](#fromName-java.lang.String) |  |
| [getName(int shapeType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int shapeType)](#toString-int) |  |
### ACCENT_BORDER_CALLOUT_1 {#ACCENT-BORDER-CALLOUT-1}
```
public static int ACCENT_BORDER_CALLOUT_1
```


Вызов границы акцента 1.

### ACCENT_BORDER_CALLOUT_2 {#ACCENT-BORDER-CALLOUT-2}
```
public static int ACCENT_BORDER_CALLOUT_2
```


Вызов границы акцента 2.

### ACCENT_BORDER_CALLOUT_3 {#ACCENT-BORDER-CALLOUT-3}
```
public static int ACCENT_BORDER_CALLOUT_3
```


Вызов границы акцента 3.

### ACCENT_BORDER_CALLOUT_90 {#ACCENT-BORDER-CALLOUT-90}
```
public static int ACCENT_BORDER_CALLOUT_90
```


Вызов границы акцента 90.

### ACCENT_CALLOUT_1 {#ACCENT-CALLOUT-1}
```
public static int ACCENT_CALLOUT_1
```


Фигура вызова акцента с одной стрелкой.

### ACCENT_CALLOUT_2 {#ACCENT-CALLOUT-2}
```
public static int ACCENT_CALLOUT_2
```


Фигура вызова акцента с двумя стрелками.

### ACCENT_CALLOUT_3 {#ACCENT-CALLOUT-3}
```
public static int ACCENT_CALLOUT_3
```


Фигура вызова акцента с тремя стрелками.

### ACCENT_CALLOUT_90 {#ACCENT-CALLOUT-90}
```
public static int ACCENT_CALLOUT_90
```


Вызов акцента 90.

### ACTION_BUTTON_BACK_PREVIOUS {#ACTION-BUTTON-BACK-PREVIOUS}
```
public static int ACTION_BUTTON_BACK_PREVIOUS
```


Кнопка действия назад предыдущий.

### ACTION_BUTTON_BEGINNING {#ACTION-BUTTON-BEGINNING}
```
public static int ACTION_BUTTON_BEGINNING
```


Кнопка действия начало.

### ACTION_BUTTON_BLANK {#ACTION-BUTTON-BLANK}
```
public static int ACTION_BUTTON_BLANK
```


Кнопка действия пустой.

### ACTION_BUTTON_DOCUMENT {#ACTION-BUTTON-DOCUMENT}
```
public static int ACTION_BUTTON_DOCUMENT
```


Кнопка действия документ.

### ACTION_BUTTON_END {#ACTION-BUTTON-END}
```
public static int ACTION_BUTTON_END
```


Кнопка действия конец.

### ACTION_BUTTON_FORWARD_NEXT {#ACTION-BUTTON-FORWARD-NEXT}
```
public static int ACTION_BUTTON_FORWARD_NEXT
```


Кнопка действия вперёд следующий.

### ACTION_BUTTON_HELP {#ACTION-BUTTON-HELP}
```
public static int ACTION_BUTTON_HELP
```


Кнопка действия справка.

### ACTION_BUTTON_HOME {#ACTION-BUTTON-HOME}
```
public static int ACTION_BUTTON_HOME
```


Кнопка действия домой.

### ACTION_BUTTON_INFORMATION {#ACTION-BUTTON-INFORMATION}
```
public static int ACTION_BUTTON_INFORMATION
```


Кнопка действия информация.

### ACTION_BUTTON_MOVIE {#ACTION-BUTTON-MOVIE}
```
public static int ACTION_BUTTON_MOVIE
```


Кнопка действия фильм.

### ACTION_BUTTON_RETURN {#ACTION-BUTTON-RETURN}
```
public static int ACTION_BUTTON_RETURN
```


Кнопка действия возврат.

### ACTION_BUTTON_SOUND {#ACTION-BUTTON-SOUND}
```
public static int ACTION_BUTTON_SOUND
```


Кнопка действия звук.

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

### BALLOON {#BALLOON}
```
public static int BALLOON
```


Шар.

### BENT_ARROW {#BENT-ARROW}
```
public static int BENT_ARROW
```


Согнутая стрелка.

### BENT_CONNECTOR_2 {#BENT-CONNECTOR-2}
```
public static int BENT_CONNECTOR_2
```


Изогнутая соединительная фигура с двумя сегментами.

### BENT_CONNECTOR_3 {#BENT-CONNECTOR-3}
```
public static int BENT_CONNECTOR_3
```


Изогнутая соединительная фигура с тремя сегментами.

### BENT_CONNECTOR_4 {#BENT-CONNECTOR-4}
```
public static int BENT_CONNECTOR_4
```


Изогнутая соединительная фигура с четырьмя сегментами.

### BENT_CONNECTOR_5 {#BENT-CONNECTOR-5}
```
public static int BENT_CONNECTOR_5
```


Изогнутая соединительная фигура с пятью сегментами.

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


Выноска границы 1.

### BORDER_CALLOUT_2 {#BORDER-CALLOUT-2}
```
public static int BORDER_CALLOUT_2
```


Выноска границы 2.

### BORDER_CALLOUT_3 {#BORDER-CALLOUT-3}
```
public static int BORDER_CALLOUT_3
```


Выноска границы 3.

### BORDER_CALLOUT_90 {#BORDER-CALLOUT-90}
```
public static int BORDER_CALLOUT_90
```


Выноска границы 90.

### BRACE_PAIR {#BRACE-PAIR}
```
public static int BRACE_PAIR
```


Пара скобок

### BRACKET_PAIR {#BRACKET-PAIR}
```
public static int BRACKET_PAIR
```


Парные квадратные скобки.

### CALLOUT_1 {#CALLOUT-1}
```
public static int CALLOUT_1
```


Фигура выноски с одной стрелкой.

### CALLOUT_2 {#CALLOUT-2}
```
public static int CALLOUT_2
```


Фигура выноски с двумя стрелками.

### CALLOUT_3 {#CALLOUT-3}
```
public static int CALLOUT_3
```


Фигура выноски с тремя стрелками.

### CALLOUT_90 {#CALLOUT-90}
```
public static int CALLOUT_90
```


Выноска 90.

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

 **Remarks:** 

Применимо только к DML‑формам.

### CHART_STAR {#CHART-STAR}
```
public static int CHART_STAR
```


Диаграмма звезда.

 **Remarks:** 

Применимо только к DML‑формам.

### CHART_X {#CHART-X}
```
public static int CHART_X
```


Диаграмма X.

 **Remarks:** 

Применимо только к DML‑формам.

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

 **Remarks:** 

Применимо только к DML‑формам.

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

 **Remarks:** 

Применимо только к DML‑формам.

### CLOUD_CALLOUT {#CLOUD-CALLOUT}
```
public static int CLOUD_CALLOUT
```


Облачная выноска.

### CORNER {#CORNER}
```
public static int CORNER
```


Угол.

 **Remarks:** 

Применимо только к DML‑формам.

### CORNER_TABS {#CORNER-TABS}
```
public static int CORNER_TABS
```


Угловые вкладки.

 **Remarks:** 

Применимо только к DML‑формам.

### CUBE {#CUBE}
```
public static int CUBE
```


Куб.

### CURVED_CONNECTOR_2 {#CURVED-CONNECTOR-2}
```
public static int CURVED_CONNECTOR_2
```


Изогнутая соединительная фигура с двумя сегментами.

### CURVED_CONNECTOR_3 {#CURVED-CONNECTOR-3}
```
public static int CURVED_CONNECTOR_3
```


Изогнутая соединительная фигура с тремя сегментами.

### CURVED_CONNECTOR_4 {#CURVED-CONNECTOR-4}
```
public static int CURVED_CONNECTOR_4
```


Изогнутая соединительная фигура с четырьмя сегментами.

### CURVED_CONNECTOR_5 {#CURVED-CONNECTOR-5}
```
public static int CURVED_CONNECTOR_5
```


Изогнутая соединительная фигура с пятью сегментами.

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

### CUSTOM_SHAPE {#CUSTOM-SHAPE}
```
public static int CUSTOM_SHAPE
```


Похоже, что этот тип формы предназначен для фигур, которые не входят в стандартный набор автофигур в Microsoft Word. Например, если вы вставляете новую автофигуру из ClipArt.

Вы не можете создавать фигуры этого типа в документе.

### DECAGON {#DECAGON}
```
public static int DECAGON
```


Десятиугольник.

 **Remarks:** 

Применимо только к DML‑формам.

### DIAGONAL_CORNERS_ROUNDED {#DIAGONAL-CORNERS-ROUNDED}
```
public static int DIAGONAL_CORNERS_ROUNDED
```


Прямоугольник с закруглённым диагональным углом.

 **Remarks:** 

Применимо только к DML‑формам.

### DIAGONAL_CORNERS_SNIPPED {#DIAGONAL-CORNERS-SNIPPED}
```
public static int DIAGONAL_CORNERS_SNIPPED
```


Прямоугольник с отрезанным диагональным углом.

 **Remarks:** 

Применимо только к DML‑формам.

### DIAGONAL_STRIPE {#DIAGONAL-STRIPE}
```
public static int DIAGONAL_STRIPE
```


Диагональная полоса.

 **Remarks:** 

Применимо только к DML‑формам.

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

 **Remarks:** 

Применимо только к DML‑формам.

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


Блок-схема: альтернативный процесс.

### FLOW_CHART_COLLATE {#FLOW-CHART-COLLATE}
```
public static int FLOW_CHART_COLLATE
```


Блок-схема: собрать.

### FLOW_CHART_CONNECTOR {#FLOW-CHART-CONNECTOR}
```
public static int FLOW_CHART_CONNECTOR
```


Блок-схема: соединитель.

### FLOW_CHART_DECISION {#FLOW-CHART-DECISION}
```
public static int FLOW_CHART_DECISION
```


Блок-схема: решение.

### FLOW_CHART_DELAY {#FLOW-CHART-DELAY}
```
public static int FLOW_CHART_DELAY
```


Блок-схема: задержка.

### FLOW_CHART_DISPLAY {#FLOW-CHART-DISPLAY}
```
public static int FLOW_CHART_DISPLAY
```


Блок-схема: отображение.

### FLOW_CHART_DOCUMENT {#FLOW-CHART-DOCUMENT}
```
public static int FLOW_CHART_DOCUMENT
```


Блок-схема: документ.

### FLOW_CHART_EXTRACT {#FLOW-CHART-EXTRACT}
```
public static int FLOW_CHART_EXTRACT
```


Блок-схема: извлечение.

### FLOW_CHART_INPUT_OUTPUT {#FLOW-CHART-INPUT-OUTPUT}
```
public static int FLOW_CHART_INPUT_OUTPUT
```


Блок-схема: ввод‑вывод.

### FLOW_CHART_INTERNAL_STORAGE {#FLOW-CHART-INTERNAL-STORAGE}
```
public static int FLOW_CHART_INTERNAL_STORAGE
```


Блок-схема: внутреннее хранилище.

### FLOW_CHART_MAGNETIC_DISK {#FLOW-CHART-MAGNETIC-DISK}
```
public static int FLOW_CHART_MAGNETIC_DISK
```


Блок-схема: магнитный диск.

### FLOW_CHART_MAGNETIC_DRUM {#FLOW-CHART-MAGNETIC-DRUM}
```
public static int FLOW_CHART_MAGNETIC_DRUM
```


Блок-схема: магнитный барабан.

### FLOW_CHART_MAGNETIC_TAPE {#FLOW-CHART-MAGNETIC-TAPE}
```
public static int FLOW_CHART_MAGNETIC_TAPE
```


Блок-схема char магнитная лента.

### FLOW_CHART_MANUAL_INPUT {#FLOW-CHART-MANUAL-INPUT}
```
public static int FLOW_CHART_MANUAL_INPUT
```


Блок-схема: ручной ввод.

### FLOW_CHART_MANUAL_OPERATION {#FLOW-CHART-MANUAL-OPERATION}
```
public static int FLOW_CHART_MANUAL_OPERATION
```


Блок-схема: ручная операция.

### FLOW_CHART_MERGE {#FLOW-CHART-MERGE}
```
public static int FLOW_CHART_MERGE
```


Блок-схема: объединение.

### FLOW_CHART_MULTIDOCUMENT {#FLOW-CHART-MULTIDOCUMENT}
```
public static int FLOW_CHART_MULTIDOCUMENT
```


Блок-схема: многодокументный.

### FLOW_CHART_OFFLINE_STORAGE {#FLOW-CHART-OFFLINE-STORAGE}
```
public static int FLOW_CHART_OFFLINE_STORAGE
```


Блок-схема: офлайн‑хранилище.

### FLOW_CHART_OFFPAGE_CONNECTOR {#FLOW-CHART-OFFPAGE-CONNECTOR}
```
public static int FLOW_CHART_OFFPAGE_CONNECTOR
```


Блок-схема: соединитель за пределами страницы.

### FLOW_CHART_ONLINE_STORAGE {#FLOW-CHART-ONLINE-STORAGE}
```
public static int FLOW_CHART_ONLINE_STORAGE
```


Блок-схема: онлайн‑хранилище.

### FLOW_CHART_OR {#FLOW-CHART-OR}
```
public static int FLOW_CHART_OR
```


Блок-схема или.

### FLOW_CHART_PREDEFINED_PROCESS {#FLOW-CHART-PREDEFINED-PROCESS}
```
public static int FLOW_CHART_PREDEFINED_PROCESS
```


Предопределенный процесс блок-схемы

### FLOW_CHART_PREPARATION {#FLOW-CHART-PREPARATION}
```
public static int FLOW_CHART_PREPARATION
```


Подготовка блок-схемы.

### FLOW_CHART_PROCESS {#FLOW-CHART-PROCESS}
```
public static int FLOW_CHART_PROCESS
```


Процесс блок-схемы.

### FLOW_CHART_PUNCHED_CARD {#FLOW-CHART-PUNCHED-CARD}
```
public static int FLOW_CHART_PUNCHED_CARD
```


Перфокарта блок-схемы.

### FLOW_CHART_PUNCHED_TAPE {#FLOW-CHART-PUNCHED-TAPE}
```
public static int FLOW_CHART_PUNCHED_TAPE
```


Перфолента блок-схемы.

### FLOW_CHART_SORT {#FLOW-CHART-SORT}
```
public static int FLOW_CHART_SORT
```


Сортировка блок-схемы.

### FLOW_CHART_SUMMING_JUNCTION {#FLOW-CHART-SUMMING-JUNCTION}
```
public static int FLOW_CHART_SUMMING_JUNCTION
```


Суммирующий узел блок-схемы.

### FLOW_CHART_TERMINATOR {#FLOW-CHART-TERMINATOR}
```
public static int FLOW_CHART_TERMINATOR
```


Терминатор блок-схемы.

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

 **Remarks:** 

Применимо только к DML‑формам.

### FUNNEL {#FUNNEL}
```
public static int FUNNEL
```


Воронка.

 **Remarks:** 

Применимо только к DML‑формам.

### GEAR_6 {#GEAR-6}
```
public static int GEAR_6
```


Шестерня с шестью зубьями.

 **Remarks:** 

Применимо только к DML‑формам.

### GEAR_9 {#GEAR-9}
```
public static int GEAR_9
```


Шестерня с девятью зубьями.

 **Remarks:** 

Применимо только к DML‑формам.

### GROUP {#GROUP}
```
public static int GROUP
```


Фигура является групповой фигурой.

### HALF_FRAME {#HALF-FRAME}
```
public static int HALF_FRAME
```


Полурама.

 **Remarks:** 

Применимо только к DML‑формам.

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

 **Remarks:** 

Применимо только к DML‑формам.

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

### IMAGE {#IMAGE}
```
public static int IMAGE
```


Фигура является изображением.

### INVERSE_LINE {#INVERSE-LINE}
```
public static int INVERSE_LINE
```


Обратная линия.

 **Remarks:** 

Применимо только к DML‑формам.

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

 **Remarks:** 

Применимо только к DML‑формам.

### LEFT_RIGHT_ARROW {#LEFT-RIGHT-ARROW}
```
public static int LEFT_RIGHT_ARROW
```


Стрелка влево‑вправо.

### LEFT_RIGHT_ARROW_CALLOUT {#LEFT-RIGHT-ARROW-CALLOUT}
```
public static int LEFT_RIGHT_ARROW_CALLOUT
```


Выноска со стрелкой влево‑вправо.

### LEFT_RIGHT_CIRCULAR_ARROW {#LEFT-RIGHT-CIRCULAR-ARROW}
```
public static int LEFT_RIGHT_CIRCULAR_ARROW
```


Круговая стрелка слева направо.

 **Remarks:** 

Применимо только к DML‑формам.

### LEFT_RIGHT_RIBBON {#LEFT-RIGHT-RIBBON}
```
public static int LEFT_RIGHT_RIBBON
```


Лента слева направо.

 **Remarks:** 

Применимо только к DML‑формам.

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

 **Remarks:** 

Применимо только к DML‑формам.

### MATH_EQUAL {#MATH-EQUAL}
```
public static int MATH_EQUAL
```


Знак равенства.

 **Remarks:** 

Применимо только к DML‑формам.

### MATH_MINUS {#MATH-MINUS}
```
public static int MATH_MINUS
```


Знак вычитания.

 **Remarks:** 

Применимо только к DML‑формам.

### MATH_MULTIPLY {#MATH-MULTIPLY}
```
public static int MATH_MULTIPLY
```


Знак умножения.

 **Remarks:** 

Применимо только к DML‑формам.

### MATH_NOT_EQUAL {#MATH-NOT-EQUAL}
```
public static int MATH_NOT_EQUAL
```


Знак неравенства.

 **Remarks:** 

Применимо только к DML‑формам.

### MATH_PLUS {#MATH-PLUS}
```
public static int MATH_PLUS
```


Знак сложения.

 **Remarks:** 

Применимо только к DML‑формам.

### MIN_VALUE {#MIN-VALUE}
```
public static int MIN_VALUE
```


Зарезервировано для использования системой.

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

 **Remarks:** 

Применимо только к DML‑формам.

### NON_PRIMITIVE {#NON-PRIMITIVE}
```
public static int NON_PRIMITIVE
```


Фигура, нарисованная пользователем и состоящая из нескольких сегментов и/или вершин (кривая, произвольная форма или каракули).

Вы не можете создавать фигуры этого типа в документе.

### NOTCHED_RIGHT_ARROW {#NOTCHED-RIGHT-ARROW}
```
public static int NOTCHED_RIGHT_ARROW
```


Стрелка вправо с вырезом.

### NO_SMOKING {#NO-SMOKING}
```
public static int NO_SMOKING
```


NoSmoking.

### OCTAGON {#OCTAGON}
```
public static int OCTAGON
```


Восьмиугольник.

### OLE_CONTROL {#OLE-CONTROL}
```
public static int OLE_CONTROL
```


Фигура является элементом управления ActiveX.

Вы не можете создавать фигуры этого типа в документе.

### OLE_OBJECT {#OLE-OBJECT}
```
public static int OLE_OBJECT
```


Фигура является объектом OLE.

Вы не можете создавать фигуры этого типа в документе.

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

 **Remarks:** 

Применимо только к DML‑формам.

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

 **Remarks:** 

Применимо только к DML‑формам.

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


Выноска с четырёхстрелочной стрелкой.

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


Выноска со стрелкой вправо

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


Закруглённый прямоугольник.

### SEAL {#SEAL}
```
public static int SEAL
```


Печать.

### SEAL_10 {#SEAL-10}
```
public static int SEAL_10
```


Звезда с десятью лучами.

 **Remarks:** 

Применимо только к DML‑формам.

### SEAL_12 {#SEAL-12}
```
public static int SEAL_12
```


Звезда с двенадцатью лучами.

 **Remarks:** 

Применимо только к DML‑формам.

### SEAL_16 {#SEAL-16}
```
public static int SEAL_16
```


Звезда с шестнадцатью лучами.

### SEAL_24 {#SEAL-24}
```
public static int SEAL_24
```


Звезда с 24 лучами.

### SEAL_32 {#SEAL-32}
```
public static int SEAL_32
```


Звезда с 32 лучами.

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

 **Remarks:** 

Применимо только к DML‑формам.

### SEAL_7 {#SEAL-7}
```
public static int SEAL_7
```


Звезда с семью лучами.

 **Remarks:** 

Применимо только к DML‑формам.

### SEAL_8 {#SEAL-8}
```
public static int SEAL_8
```


Звезда с восемью лучами.

### SINGLE_CORNER_ROUNDED {#SINGLE-CORNER-ROUNDED}
```
public static int SINGLE_CORNER_ROUNDED
```


Прямоугольник с одной скруглённой стороной.

 **Remarks:** 

Применимо только к DML‑формам.

### SINGLE_CORNER_SNIPPED {#SINGLE-CORNER-SNIPPED}
```
public static int SINGLE_CORNER_SNIPPED
```


Объект с вырезанным углом у прямоугольника.

 **Remarks:** 

Применимо только к DML‑формам.

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

 **Remarks:** 

Применимо только к DML‑формам.

### STAR {#STAR}
```
public static int STAR
```


Звезда.

### STRAIGHT_CONNECTOR_1 {#STRAIGHT-CONNECTOR-1}
```
public static int STRAIGHT_CONNECTOR_1
```


Прямая соединительная фигура.

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

 **Remarks:** 

Применимо только к DML‑формам.

### TEARDROP {#TEARDROP}
```
public static int TEARDROP
```


Капля.

 **Remarks:** 

Применимо только к DML‑формам.

### TEXT_ARCH_DOWN_CURVE {#TEXT-ARCH-DOWN-CURVE}
```
public static int TEXT_ARCH_DOWN_CURVE
```


Арка вниз, объект WordArt.

### TEXT_ARCH_DOWN_POUR {#TEXT-ARCH-DOWN-POUR}
```
public static int TEXT_ARCH_DOWN_POUR
```


Арка вниз, заливка, объект WordArt.

### TEXT_ARCH_UP_CURVE {#TEXT-ARCH-UP-CURVE}
```
public static int TEXT_ARCH_UP_CURVE
```


Арка вверх, объект WordArt.

### TEXT_ARCH_UP_POUR {#TEXT-ARCH-UP-POUR}
```
public static int TEXT_ARCH_UP_POUR
```


Арка вверх, заливка, объект WordArt.

### TEXT_BOX {#TEXT-BOX}
```
public static int TEXT_BOX
```


Фигура является текстовым полем. Обратите внимание, что фигуры многих других типов также могут содержать текст. Фигура не обязана быть этого типа, чтобы содержать текст.

### TEXT_BUTTON_CURVE {#TEXT-BUTTON-CURVE}
```
public static int TEXT_BUTTON_CURVE
```


Кнопка кривая, объект WordArt.

### TEXT_BUTTON_POUR {#TEXT-BUTTON-POUR}
```
public static int TEXT_BUTTON_POUR
```


Кнопка заливка, объект WordArt.

### TEXT_CAN_DOWN {#TEXT-CAN-DOWN}
```
public static int TEXT_CAN_DOWN
```


Банка вниз, объект WordArt.

### TEXT_CAN_UP {#TEXT-CAN-UP}
```
public static int TEXT_CAN_UP
```


Банка вверх, объект WordArt.

### TEXT_CASCADE_DOWN {#TEXT-CASCADE-DOWN}
```
public static int TEXT_CASCADE_DOWN
```


Каскад вниз, объект WordArt.

### TEXT_CASCADE_UP {#TEXT-CASCADE-UP}
```
public static int TEXT_CASCADE_UP
```


Каскад вверх, объект WordArt.

### TEXT_CHEVRON {#TEXT-CHEVRON}
```
public static int TEXT_CHEVRON
```


Шеврон, объект WordArt.

### TEXT_CHEVRON_INVERTED {#TEXT-CHEVRON-INVERTED}
```
public static int TEXT_CHEVRON_INVERTED
```


Шеврон перевёрнутый, объект WordArt.

### TEXT_CIRCLE_CURVE {#TEXT-CIRCLE-CURVE}
```
public static int TEXT_CIRCLE_CURVE
```


Круг кривая, объект WordArt.

### TEXT_CIRCLE_POUR {#TEXT-CIRCLE-POUR}
```
public static int TEXT_CIRCLE_POUR
```


Круг заливка, объект WordArt.

### TEXT_CURVE {#TEXT-CURVE}
```
public static int TEXT_CURVE
```


Текстовая кривая.

### TEXT_CURVE_DOWN {#TEXT-CURVE-DOWN}
```
public static int TEXT_CURVE_DOWN
```


Кривая вниз, объект WordArt.

### TEXT_CURVE_UP {#TEXT-CURVE-UP}
```
public static int TEXT_CURVE_UP
```


Кривая вверх, объект WordArt.

### TEXT_DEFLATE {#TEXT-DEFLATE}
```
public static int TEXT_DEFLATE
```


Сжать, объект WordArt.

### TEXT_DEFLATE_BOTTOM {#TEXT-DEFLATE-BOTTOM}
```
public static int TEXT_DEFLATE_BOTTOM
```


Сжать снизу, объект WordArt.

### TEXT_DEFLATE_INFLATE {#TEXT-DEFLATE-INFLATE}
```
public static int TEXT_DEFLATE_INFLATE
```


Сжать развернуть, объект WordArt.

### TEXT_DEFLATE_INFLATE_DEFLATE {#TEXT-DEFLATE-INFLATE-DEFLATE}
```
public static int TEXT_DEFLATE_INFLATE_DEFLATE
```


Сжать развернуть сжать, объект WordArt.

### TEXT_DEFLATE_TOP {#TEXT-DEFLATE-TOP}
```
public static int TEXT_DEFLATE_TOP
```


Сжать сверху, объект WordArt.

### TEXT_FADE_DOWN {#TEXT-FADE-DOWN}
```
public static int TEXT_FADE_DOWN
```


Исчезать вниз, объект WordArt.

### TEXT_FADE_LEFT {#TEXT-FADE-LEFT}
```
public static int TEXT_FADE_LEFT
```


Исчезать влево, объект WordArt.

### TEXT_FADE_RIGHT {#TEXT-FADE-RIGHT}
```
public static int TEXT_FADE_RIGHT
```


Исчезать вправо, объект WordArt.

### TEXT_FADE_UP {#TEXT-FADE-UP}
```
public static int TEXT_FADE_UP
```


Исчезать вверх, объект WordArt.

### TEXT_HEXAGON {#TEXT-HEXAGON}
```
public static int TEXT_HEXAGON
```


Текст шестиугольник.

### TEXT_INFLATE {#TEXT-INFLATE}
```
public static int TEXT_INFLATE
```


Раздуть, объект WordArt.

### TEXT_INFLATE_BOTTOM {#TEXT-INFLATE-BOTTOM}
```
public static int TEXT_INFLATE_BOTTOM
```


Раздуть снизу, объект WordArt.

### TEXT_INFLATE_TOP {#TEXT-INFLATE-TOP}
```
public static int TEXT_INFLATE_TOP
```


Раздуть сверху, объект WordArt.

### TEXT_OCTAGON {#TEXT-OCTAGON}
```
public static int TEXT_OCTAGON
```


Текст восьмиугольник.

### TEXT_ON_CURVE {#TEXT-ON-CURVE}
```
public static int TEXT_ON_CURVE
```


Текст по кривой.

### TEXT_ON_RING {#TEXT-ON-RING}
```
public static int TEXT_ON_RING
```


Текст по кольцу.

### TEXT_PLAIN_TEXT {#TEXT-PLAIN-TEXT}
```
public static int TEXT_PLAIN_TEXT
```


Простой текст, объект WordArt.

### TEXT_RING {#TEXT-RING}
```
public static int TEXT_RING
```


Текстовое кольцо.

### TEXT_RING_INSIDE {#TEXT-RING-INSIDE}
```
public static int TEXT_RING_INSIDE
```


Кольцо внутри, объект WordArt.

### TEXT_RING_OUTSIDE {#TEXT-RING-OUTSIDE}
```
public static int TEXT_RING_OUTSIDE
```


Кольцо снаружи, объект WordArt.

### TEXT_SIMPLE {#TEXT-SIMPLE}
```
public static int TEXT_SIMPLE
```


Простой текст.

### TEXT_SLANT_DOWN {#TEXT-SLANT-DOWN}
```
public static int TEXT_SLANT_DOWN
```


Наклон вниз, объект WordArt.

### TEXT_SLANT_UP {#TEXT-SLANT-UP}
```
public static int TEXT_SLANT_UP
```


Наклон вверх, объект WordArt.

### TEXT_STOP {#TEXT-STOP}
```
public static int TEXT_STOP
```


Стоп, объект WordArt.

### TEXT_TRIANGLE {#TEXT-TRIANGLE}
```
public static int TEXT_TRIANGLE
```


Треугольник, объект WordArt.

### TEXT_TRIANGLE_INVERTED {#TEXT-TRIANGLE-INVERTED}
```
public static int TEXT_TRIANGLE_INVERTED
```


Перевернутый треугольник, объект WordArt.

### TEXT_WAVE {#TEXT-WAVE}
```
public static int TEXT_WAVE
```


Текстовая волна.

### TEXT_WAVE_1 {#TEXT-WAVE-1}
```
public static int TEXT_WAVE_1
```


Волна 1, объект WordArt.

### TEXT_WAVE_2 {#TEXT-WAVE-2}
```
public static int TEXT_WAVE_2
```


Волна 2, объект WordArt.

### TEXT_WAVE_3 {#TEXT-WAVE-3}
```
public static int TEXT_WAVE_3
```


Волна 3, объект WordArt.

### TEXT_WAVE_4 {#TEXT-WAVE-4}
```
public static int TEXT_WAVE_4
```


Волна 4, объект WordArt.

### THICK_ARROW {#THICK-ARROW}
```
public static int THICK_ARROW
```


Толстая стрелка.

### TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED {#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED}
```
public static int TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED
```


Прямоугольник с отрезанным и скруглённым одним углом.

 **Remarks:** 

Применимо только к DML‑формам.

### TOP_CORNERS_ROUNDED {#TOP-CORNERS-ROUNDED}
```
public static int TOP_CORNERS_ROUNDED
```


Прямоугольник с закругленным углом одной стороны.

 **Remarks:** 

Применимо только к DML‑формам.

### TOP_CORNERS_SNIPPED {#TOP-CORNERS-SNIPPED}
```
public static int TOP_CORNERS_SNIPPED
```


Прямоугольник с отрезанным углом одной стороны.

 **Remarks:** 

Применимо только к DML‑формам.

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


Врезка со стрелкой вверх.

### UP_DOWN_ARROW {#UP-DOWN-ARROW}
```
public static int UP_DOWN_ARROW
```


Стрелка вверх‑вниз.

### UP_DOWN_ARROW_CALLOUT {#UP-DOWN-ARROW-CALLOUT}
```
public static int UP_DOWN_ARROW_CALLOUT
```


Врезка со стрелкой вверх‑вниз.

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


Врезка в виде клина эллипса.

### WEDGE_PIE {#WEDGE-PIE}
```
public static int WEDGE_PIE
```


Секторный круг.

 **Remarks:** 

Применимо только к DML‑формам.

### WEDGE_RECT_CALLOUT {#WEDGE-RECT-CALLOUT}
```
public static int WEDGE_RECT_CALLOUT
```


Врезка в виде клина прямоугольника.

### WEDGE_R_RECT_CALLOUT {#WEDGE-R-RECT-CALLOUT}
```
public static int WEDGE_R_RECT_CALLOUT
```


Врезка в виде клина R‑прямоугольника.

### length {#length}
```
public static int length
```


### fromName(String shapeTypeName) {#fromName-java.lang.String}
```
public static int fromName(String shapeTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| shapeTypeName | java.lang.String |  |

**Returns:**
int
### getName(int shapeType) {#getName-int}
```
public static String getName(int shapeType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| shapeType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int shapeType) {#toString-int}
```
public static String toString(int shapeType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| shapeType | int |  |

**Returns:**
java.lang.String
