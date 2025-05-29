---
title: ShapeType Enum
linktitle: ShapeType
articleTitle: ShapeType
second_title: Aspose.Words для .NET
description: Изучите перечисление Aspose.Words.Drawing.ShapeType, чтобы определять и настраивать типы фигур в документах Microsoft Word для повышения визуальной привлекательности.
type: docs
weight: 1690
url: /ru/net/aspose.words.drawing/shapetype/
---
## ShapeType enumeration

Указывает тип фигуры в документе Microsoft Word.

```csharp
public enum ShapeType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Image | `75` | Форма — это изображение. |
| TextBox | `202` | Фигура — это текстовое поле. Обратите внимание, что фигуры многих других типов также могут иметь текст внутри себя. Фигура не обязательно должна иметь этот тип, чтобы содержать текст. |
| Group | `-1` | Форма представляет собой групповую форму. |
| OleObject | `-2` | Фигура является объектом OLE. |
| OleControl | `201` | Фигура представляет собой элемент управления ActiveX. |
| NonPrimitive | `0` | Фигура, нарисованная пользователем и состоящая из нескольких сегментов и/или вершин (кривая, произвольная форма или каракули). |
| Rectangle | `1` | Прямоугольник. |
| RoundRectangle | `2` | Круглый прямоугольник. |
| Ellipse | `3` | Эллипс. |
| Diamond | `4` | Алмаз. |
| Triangle | `5` | Треугольник. |
| RightTriangle | `6` | Прямоугольный треугольник. |
| Parallelogram | `7` | Параллелограмм. |
| Trapezoid | `8` | Трапеция. |
| Hexagon | `9` | Шестиугольник. |
| Octagon | `10` | Восьмиугольник. |
| Plus | `11` | Плюс. |
| Star | `12` | Звезда. |
| Arrow | `13` | Стрелка. |
| ThickArrow | `14` | Толстая стрелка. |
| HomePlate | `15` | Домашняя пластина. |
| Cube | `16` | Куб. |
| Balloon | `17` | Воздушный шар. |
| Seal | `18` | Печать. |
| Arc | `19` | Дуга. |
| Line | `20` | Строка. |
| Plaque | `21` | Бляшка. |
| Can | `22` | Кан. |
| Donut | `23` | Пончик. |
| TextSimple | `24` | Текст простой. |
| TextOctagon | `25` | Текстовый восьмиугольник. |
| TextHexagon | `26` | Текстовый шестиугольник. |
| TextCurve | `27` | Текстовая кривая. |
| TextWave | `28` | Текстовая волна. |
| TextRing | `29` | Текстовое кольцо. |
| TextOnCurve | `30` | Текст на кривой. |
| TextOnRing | `31` | Текст на кольце. |
| StraightConnector1 | `32` | Форма прямого соединителя. |
| BentConnector2 | `33` | Изогнутая соединительная форма с двумя сегментами. |
| BentConnector3 | `34` | Изогнутая соединительная форма с тремя сегментами. |
| BentConnector4 | `35` | Изогнутая соединительная форма с четырьмя сегментами. |
| BentConnector5 | `36` | Изогнутая соединительная форма с пятью сегментами. |
| CurvedConnector2 | `37` | Изогнутая форма соединителя с двумя сегментами. |
| CurvedConnector3 | `38` | Изогнутая форма соединителя с тремя сегментами. |
| CurvedConnector4 | `39` | Изогнутая форма соединителя с четырьмя сегментами. |
| CurvedConnector5 | `40` | Изогнутая форма соединителя с пятью сегментами. |
| Callout1 | `41` | Выноска с одной стрелкой. |
| Callout2 | `42` | Выноска с двумя стрелками. |
| Callout3 | `43` | Выноска с тремя стрелками. |
| AccentCallout1 | `44` | Выноска с акцентом и одной стрелкой. |
| AccentCallout2 | `45` | Выноска с акцентом и двумя стрелками. |
| AccentCallout3 | `46` | Выноска с тремя стрелками. |
| BorderCallout1 | `47` | Выноска границы 1. |
| BorderCallout2 | `48` | Выноска границы 2. |
| BorderCallout3 | `49` | Выноска границы 3. |
| AccentBorderCallout1 | `50` | Выноска акцентной границы 1. |
| AccentBorderCallout2 | `51` | Выноска акцентной границы 2. |
| AccentBorderCallout3 | `52` | Выноска акцентной границы 3. |
| Ribbon | `53` | Лента. |
| Ribbon2 | `54` | Лента 2. |
| Chevron | `55` | Шеврон. |
| Pentagon | `56` | Пентагон. |
| NoSmoking | `57` | Некурящий. |
| Seal8 | `58` | Восьмиконечная звезда. |
| Seal16 | `59` | 16-конечная звезда. |
| Seal32 | `60` | 32-конечная звезда. |
| WedgeRectCallout | `61` | Выноска клиновидного прямоугольника. |
| WedgeRRectCallout | `62` | Прямоугольная выноска клина R. |
| WedgeEllipseCallout | `63` | Выноска клиновидного эллипса. |
| Wave | `64` | Волна. |
| FoldedCorner | `65` | Загнутый уголок. |
| LeftArrow | `66` | Стрелка влево. |
| DownArrow | `67` | Стрелка вниз. |
| UpArrow | `68` | Стрелка вверх. |
| LeftRightArrow | `69` | Стрелка влево-вправо. |
| UpDownArrow | `70` | Стрелка вверх-вниз. |
| IrregularSeal1 | `71` | Неправильная прокладка 1. |
| IrregularSeal2 | `72` | Неправильное уплотнение 2. |
| LightningBolt | `73` | Молния. |
| Heart | `74` | Сердце. |
| QuadArrow | `76` | Квадратная стрелка. |
| LeftArrowCallout | `77` | Выноска со стрелкой влево. |
| RightArrowCallout | `78` | Выноска со стрелкой вправо |
| UpArrowCallout | `79` | Выноска со стрелкой вверх. |
| DownArrowCallout | `80` | Выноска со стрелкой вниз. |
| LeftRightArrowCallout | `81` | Выноска со стрелкой влево-вправо. |
| UpDownArrowCallout | `82` | Выноска со стрелкой вверх-вниз. |
| QuadArrowCallout | `83` | Выноска с четырехугольной стрелкой. |
| Bevel | `84` | Скос. |
| LeftBracket | `85` | Левая скобка. |
| RightBracket | `86` | Правая скобка. |
| LeftBrace | `87` | Левая фигурная скобка. |
| RightBrace | `88` | Правая фигурная скобка. |
| LeftUpArrow | `89` | Стрелка влево вверх. |
| BentUpArrow | `90` | Изогнутая стрелка вверх. |
| BentArrow | `91` | Изогнутая стрела. |
| Seal24 | `92` | 24-конечная звезда. |
| StripedRightArrow | `93` | Полосатая стрелка вправо. |
| NotchedRightArrow | `94` | Стрелка вправо с зазубринами. |
| BlockArc | `95` | Блокировать дугу. |
| SmileyFace | `96` | Смайлик. |
| VerticalScroll | `97` | Вертикальная прокрутка. |
| HorizontalScroll | `98` | Горизонтальная прокрутка. |
| CircularArrow | `99` | Круговая стрелка. |
| CustomShape | `100` | Этот тип фигуры, похоже, установлен для фигур, которые не являются частью стандартного набора автофигур в Microsoft Word. Например, если вы вставляете новую автофигуру из ClipArt. |
| UturnArrow | `101` | Стрелка поворота. |
| CurvedRightArrow | `102` | Изогнутая стрелка вправо. |
| CurvedLeftArrow | `103` | Изогнутая левая стрелка. |
| CurvedUpArrow | `104` | Изогнутая стрелка вверх |
| CurvedDownArrow | `105` | Изогнутая стрелка вниз. |
| CloudCallout | `106` | Выноска облака. |
| EllipseRibbon | `107` | Лента эллипса. |
| EllipseRibbon2 | `108` | Эллипсовая лента 2. |
| FlowChartProcess | `109` | Схема процесса. |
| FlowChartDecision | `110` | Схема решения. |
| FlowChartInputOutput | `111` | Блок-схема вход-выход. |
| FlowChartPredefinedProcess | `112` | Блок-схема предопределенного процесса |
| FlowChartInternalStorage | `113` | Блок-схема внутреннего хранилища. |
| FlowChartDocument | `114` | Документ блок-схемы. |
| FlowChartMultidocument | `115` | Блок-схема для нескольких документов. |
| FlowChartTerminator | `116` | Блок-схема терминатора. |
| FlowChartPreparation | `117` | Подготовка блок-схемы. |
| FlowChartManualInput | `118` | Блок-схема ручного ввода. |
| FlowChartManualOperation | `119` | Блок-схема ручного управления. |
| FlowChartConnector | `120` | Соединительная схема. |
| FlowChartPunchedCard | `121` | Перфокарта блок-схемы. |
| FlowChartPunchedTape | `122` | Блок-схема перфоленты. |
| FlowChartSummingJunction | `123` | Схема суммирования узлов. |
| FlowChartOr | `124` | Блок-схема или. |
| FlowChartCollate | `125` | Схема последовательности операций. |
| FlowChartSort | `126` | Сортировка блок-схемы. |
| FlowChartExtract | `127` | Извлечение блок-схемы. |
| FlowChartMerge | `128` | Слияние блок-схем. |
| FlowChartOfflineStorage | `129` | Схема офлайн-хранения. |
| FlowChartOnlineStorage | `130` | Схема онлайн-хранения. |
| FlowChartMagneticTape | `131` | Магнитная лента Flow Char. |
| FlowChartMagneticDisk | `132` | Блок-схема магнитного диска. |
| FlowChartMagneticDrum | `133` | Схема магнитного барабана. |
| FlowChartDisplay | `134` | Отображение блок-схемы. |
| FlowChartDelay | `135` | Задержка блок-схемы. |
| TextPlainText | `136` | Обычный текст, объект WordArt. |
| TextStop | `137` | Стоп, объект WordArt. |
| TextTriangle | `138` | Треугольник, объект WordArt. |
| TextTriangleInverted | `139` | Треугольник перевернутый, объект WordArt. |
| TextChevron | `140` | Шеврон, объект WordArt. |
| TextChevronInverted | `141` | Перевернутый шеврон, объект WordArt. |
| TextRingInside | `142` | Кольцо внутри, объект WordArt. |
| TextRingOutside | `143` | Кольцо снаружи, объект WordArt. |
| TextArchUpCurve | `144` | Дуга вверх, кривая, объект WordArt. |
| TextArchDownCurve | `145` | Дуга вниз, кривая, объект WordArt. |
| TextCircleCurve | `146` | Круглая кривая, объект WordArt. |
| TextButtonCurve | `147` | Кривая кнопки, объект WordArt. |
| TextArchUpPour | `148` | Заливка арки, объект WordArt. |
| TextArchDownPour | `149` | Арочный слив, объект WordArt. |
| TextCirclePour | `150` | Круглая заливка, объект WordArt. |
| TextButtonPour | `151` | Кнопка заливки, объект WordArt. |
| TextCurveUp | `152` | Изгиб вверх, объект WordArt. |
| TextCurveDown | `153` | Кривая вниз, объект WordArt. |
| TextCascadeUp | `154` | Каскад вверх, объект WordArt. |
| TextCascadeDown | `155` | Каскад вниз, объект WordArt. |
| TextWave1 | `156` | Волна 1, объект WordArt. |
| TextWave2 | `157` | Волна 2, объект WordArt. |
| TextWave3 | `158` | Волна 3, объект WordArt. |
| TextWave4 | `159` | Волна 4, объект WordArt. |
| TextInflate | `160` | Раздуть, объект WordArt. |
| TextDeflate | `161` | Сдуть, объект WordArt. |
| TextInflateBottom | `162` | Раздуть дно, объект WordArt. |
| TextDeflateBottom | `163` | Сдуть дно, объект WordArt. |
| TextInflateTop | `164` | Раздутый верх, объект WordArt. |
| TextDeflateTop | `165` | Сбросить верхнюю часть, объект WordArt. |
| TextDeflateInflate | `166` | Сдуть, раздуть, объект WordArt. |
| TextDeflateInflateDeflate | `167` | Сдуть, раздуть, сдуть, объект WordArt. |
| TextFadeRight | `168` | Плавный переход вправо, объект WordArt. |
| TextFadeLeft | `169` | Исчезновение влево, объект WordArt. |
| TextFadeUp | `170` | Плавное появление, объект WordArt. |
| TextFadeDown | `171` | Затухание, объект WordArt. |
| TextSlantUp | `172` | Наклон вверх, объект WordArt. |
| TextSlantDown | `173` | Наклон вниз, объект WordArt. |
| TextCanUp | `174` | Можно вверх, объект WordArt. |
| TextCanDown | `175` | Может вниз, объект WordArt. |
| FlowChartAlternateProcess | `176` | Блок-схема альтернативного процесса. |
| FlowChartOffpageConnector | `177` | Блок-схема вне страницы коннектора. |
| Callout90 | `178` | Выноска 90. |
| AccentCallout90 | `179` | Выноска акцента 90. |
| BorderCallout90 | `180` | Выноска границы 90. |
| AccentBorderCallout90 | `181` | Выноска акцентной границы 90. |
| LeftRightUpArrow | `182` | Стрелка влево-вправо-вверх. |
| Sun | `183` | Вс. |
| Moon | `184` | Луна. |
| BracketPair | `185` | Пара кронштейнов. |
| BracePair | `186` | Пара скобок |
| Seal4 | `187` | Четырехконечная звезда. |
| DoubleWave | `188` | Двойная волна. |
| ActionButtonBlank | `189` | Кнопка действия пустая. |
| ActionButtonHome | `190` | Кнопка действия домой. |
| ActionButtonHelp | `191` | Справка по кнопке действия. |
| ActionButtonInformation | `192` | Информация о кнопке действия. |
| ActionButtonForwardNext | `193` | Кнопка действия вперед далее. |
| ActionButtonBackPrevious | `194` | Кнопка действия назад назад. |
| ActionButtonEnd | `195` | Кнопка действия конец. |
| ActionButtonBeginning | `196` | Начало действия кнопки. |
| ActionButtonReturn | `197` | Кнопка действия возврата. |
| ActionButtonDocument | `198` | Кнопка действия document. |
| ActionButtonSound | `199` | Звук кнопки действия. |
| ActionButtonMovie | `200` | Кнопка действия фильм. |
| SingleCornerSnipped | `203` | Вырезать один угол прямоугольного объекта. |
| TopCornersSnipped | `204` | Вырезать прямоугольник с той же стороны угла. |
| DiagonalCornersSnipped | `205` | Разрезать диагональный угол прямоугольника. |
| TopCornersOneRoundedOneSnipped | `206` | Вырезать и скруглить прямоугольник с одним углом. |
| SingleCornerRounded | `207` | Прямоугольник с закругленным одним углом. |
| TopCornersRounded | `208` | Прямоугольник с закругленными углами с той же стороны. |
| DiagonalCornersRounded | `209` | Прямоугольник с закругленными углами и диагональю. |
| Heptagon | `210` | Семиугольник. |
| Cloud | `211` | Облако. |
| Seal6 | `212` | Шестиконечная звезда. |
| Seal7 | `213` | Семиконечная звезда. |
| Seal10 | `214` | Десятиконечная звезда. |
| Seal12 | `215` | Двенадцатиконечная звезда. |
| SwooshArrow | `216` | Стрелка свистка. |
| Teardrop | `217` | Слеза. |
| SquareTabs | `218` | Квадратные вкладки. |
| PlaqueTabs | `219` | Вкладки для зубных бляшек. |
| Pie | `220` | Пирог. |
| WedgePie | `221` | Клиновый пирог. |
| InverseLine | `222` | Обратная линия. |
| MathPlus | `223` | Математика плюс. |
| MathMinus | `224` | Математический минус. |
| MathMultiply | `225` | Математическое умножение. |
| MathDivide | `226` | Математическое деление. |
| MathEqual | `227` | Математическое равно. |
| MathNotEqual | `228` | Математическое неравенство. |
| NonIsoscelesTrapezoid | `229` | Неравнобедренная трапеция. |
| LeftRightCircularArrow | `230` | Круговая стрелка влево-вправо. |
| LeftRightRibbon | `231` | Лента левая-правая. |
| LeftCircularArrow | `232` | Левая круговая стрелка. |
| Frame | `233` | Кадр. |
| HalfFrame | `234` | Полукадр. |
| Funnel | `235` | Воронка. |
| Gear6 | `236` | Шестизубчатая шестерня. |
| Gear9 | `237` | Девятизубая шестерня. |
| Decagon | `238` | Декагон. |
| Dodecagon | `239` | Двенадцатиугольник. |
| DiagonalStripe | `240` | Диагональная полоса. |
| Corner | `241` | Угол. |
| CornerTabs | `242` | Угловые вкладки. |
| Chord | `243` | Аккорд. |
| ChartPlus | `244` | Диаграмма плюс. |
| ChartStar | `245` | Карта звезд. |
| ChartX | `246` | Диаграмма X. |
| MinValue | `-2` | Зарезервировано для использования системой. |

## Примеры

Показывает, как вставить в документ фигуру с изображением из локальной файловой системы.

```csharp
Document doc = new Document();

// Открытый конструктор класса "Shape" создаст фигуру с типом разметки "ShapeMarkupLanguage.Vml".
// Если вам нужно создать фигуру не примитивного типа, например SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded или DiagonalCornersRounded,
// пожалуйста, используйте DocumentBuilder.InsertShape.
Shape shape = new Shape(doc, ShapeType.Image);
shape.ImageData.SetImage(ImageDir + "Windows MetaFile.wmf");
shape.Width = 100;
shape.Height = 100;

doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

doc.Save(ArtifactsDir + "Image.FromFile.docx");
```

Показывает, как Aspose.Words идентифицирует фигуры.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertShape(ShapeType.Heptagon, RelativeHorizontalPosition.Page, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

builder.InsertShape(ShapeType.Cloud, RelativeHorizontalPosition.RightMargin, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

builder.InsertShape(ShapeType.MathPlus, RelativeHorizontalPosition.RightMargin, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

// Для правильной идентификации типов фигур необходимо работать с фигурами как с DML.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx)
{
    // Соответствие «Строгее» или «Переходное» позволяет сохранить форму как DML.
    Compliance = OoxmlCompliance.Iso29500_2008_Transitional
};

doc.Save(ArtifactsDir + "Shape.ShapeTypes.docx", saveOptions);
doc = new Document(ArtifactsDir + "Shape.ShapeTypes.docx");

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

foreach (Shape shape in shapes)
{
    Console.WriteLine(shape.ShapeType);
}
```

### Смотрите также

* property [ShapeType](../shapebase/shapetype/)
* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
