---
title: "Aspose::Words::Drawing::ShapeType перечисление"
linktitle: "ShapeType"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::ShapeType перечисление. Указывает тип формы в документе Microsoft Word на C++."
type: docs
weight: 38000
url: /ru/cpp/aspose.words.drawing/shapetype/
---
## ShapeType enum


Указывает тип фигуры в документе Microsoft Word.

```cpp
enum class ShapeType
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Image | 75 | Форма является изображением. |
| TextBox | 202 | Форма является текстовым полем. Обратите внимание, что формы многих других типов также могут содержать текст внутри. Форма не обязана быть этого типа, чтобы содержать текст. |
| Group | -1 | Форма является групповой формой. |
| OleObject | -2 | Фигура является объектом OLE. Вы не можете создавать фигуры этого типа в документе. |
| OleControl | 201 | Фигура является элементом управления ActiveX. Вы не можете создавать фигуры этого типа в документе. |
| NonPrimitive | 0 | Фигура, нарисованная пользователем и состоящая из нескольких сегментов и/или вершин (кривая, произвольная форма или каракули). Вы не можете создавать фигуры этого типа в документе. |
| Rectangle | 1 | Прямоугольник. |
| RoundRectangle | 2 | Закруглённый прямоугольник. |
| Ellipse | 3 | Эллипс. |
| Diamond | 4 | Ромб. |
| Triangle | 5 | Треугольник. |
| RightTriangle | 6 | Прямоугольный треугольник. |
| Parallelogram | 7 | Параллелограмм. |
| Trapezoid | 8 | Трапеция. |
| Hexagon | 9 | Шестиугольник. |
| Octagon | 10 | Восьмиугольник. |
| Плюс | 11 | Плюс. |
| Звезда | 12 | Звезда. |
| Стрелка | 13 | Стрелка. |
| ТолстаяСтрелка | 14 | Толстая стрелка. |
| ДомашняяПлатформа | 15 | Домашняя плита. |
| Куб | 16 | Куб. |
| Шар | 17 | Шар. |
| Печать | 18 | Печать. |
| Дуга | 19 | Дуга. |
| Линия | 20 | Линия. |
| Пластина | 21 | Пластина. |
| Банка | 22 | Банка. |
| Пончик | 23 | Пончик. |
| TextSimple | 24 | Текст простой. |
| TextOctagon | 25 | Текст восьмиугольник. |
| TextHexagon | 26 | Текст шестиугольник. |
| TextCurve | 27 | Текст кривая. |
| TextWave | 28 | Текст волна. |
| TextRing | 29 | Текст кольцо. |
| TextOnCurve | 30 | Текст на кривой. |
| TextOnRing | 31 | Текст на кольце. |
| StraightConnector1 | 32 | Прямая соединительная фигура. |
| BentConnector2 | 33 | Изогнутая соединительная фигура с двумя сегментами. |
| BentConnector3 | 34 | Изогнутая соединительная фигура с тремя сегментами. |
| BentConnector4 | 35 | Изогнутая соединительная фигура с четырьмя сегментами. |
| BentConnector5 | 36 | Изогнутая соединительная фигура с пятью сегментами. |
| CurvedConnector2 | 37 | Изогнутая соединительная фигура с двумя сегментами. |
| CurvedConnector3 | 38 | Изогнутая соединительная фигура с тремя сегментами. |
| CurvedConnector4 | 39 | Изогнутая соединительная фигура с четырьмя сегментами. |
| CurvedConnector5 | 40 | Изогнутая соединительная фигура с пятью сегментами. |
| Callout1 | 41 | Фигура выноски с одной стрелкой. |
| Callout2 | 42 | Фигура выноски с двумя стрелками. |
| Callout3 | 43 | Фигура выноски с тремя стрелками. |
| AccentCallout1 | 44 | Фигура акцентной выноски с одной стрелкой. |
| AccentCallout2 | 45 | Фигура акцентной выноски с двумя стрелками. |
| AccentCallout3 | 46 | Фигура акцентной выноски с тремя стрелками. |
| BorderCallout1 | 47 | [Border](../../aspose.words/border/) выноска 1. |
| BorderCallout2 | 48 | [Border](../../aspose.words/border/) выноска 2. |
| BorderCallout3 | 49 | [Border](../../aspose.words/border/) выноска 3. |
| AccentBorderCallout1 | 50 | Вызов границы акцента 1. |
| AccentBorderCallout2 | 51 | Вызов границы акцента 2. |
| AccentBorderCallout3 | 52 | Вызов границы акцента 3. |
| Ribbon | 53 | Лента. |
| Ribbon2 | 54 | Лента 2. |
| Chevron | 55 | Шеврон. |
| Pentagon | 56 | Пятиугольник. |
| NoSmoking | 57 | Запрет курения. |
| Seal8 | 58 | Восьмиконечная звезда. |
| Seal16 | 59 | Шестнадцатиконечная звезда. |
| Seal32 | 60 | Звезда с 32 лучами. |
| WedgeRectCallout | 61 | Вызов клина прямоугольника. |
| WedgeRRectCallout | 62 | Wedge R rect выноска. |
| WedgeEllipseCallout | 63 | Wedge ellipse выноска. |
| Волна | 64 | Волна. |
| FoldedCorner | 65 | Сложенный угол. |
| LeftArrow | 66 | Стрелка влево. |
| DownArrow | 67 | Стрелка вниз. |
| UpArrow | 68 | Стрелка вверх. |
| LeftRightArrow | 69 | Стрелка влево-вправо. |
| UpDownArrow | 70 | Стрелка вверх-вниз. |
| IrregularSeal1 | 71 | Неправильная печать 1. |
| IrregularSeal2 | 72 | Неправильная печать 2. |
| LightningBolt | 73 | Молния. |
| Heart | 74 | Сердце. |
| QuadArrow | 76 | Квадратная стрелка. |
| LeftArrowCallout | 77 | Выноска левой стрелки. |
| RightArrowCallout | 78 | Выноска правой стрелки. |
| UpArrowCallout | 79 | Выноска верхней стрелки. |
| DownArrowCallout | 80 | Выноска нижней стрелки. |
| LeftRightArrowCallout | 81 | Выноска левой‑правой стрелки. |
| UpDownArrowCallout | 82 | Выноска верхней‑нижней стрелки. |
| QuadArrowCallout | 83 | Выноска квадратной стрелки. |
| Фаска | 84 | Фаска. |
| LeftBracket | 85 | Левая скобка. |
| RightBracket | 86 | Правая скобка. |
| LeftBrace | 87 | Левая фигурная скобка. |
| RightBrace | 88 | Правая фигурная скобка. |
| LeftUpArrow | 89 | Стрелка влево вверх. |
| BentUpArrow | 90 | Согнутая стрелка вверх. |
| BentArrow | 91 | Согнутая стрелка. |
| Seal24 | 92 | Звезда с 24 лучами. |
| StripedRightArrow | 93 | Полосатая стрелка вправо. |
| NotchedRightArrow | 94 | Зазубренная стрелка вправо. |
| BlockArc | 95 | Блочная дуга. |
| SmileyFace | 96 | Смайлик. |
| VerticalScroll | 97 | Вертикальная прокрутка. |
| HorizontalScroll | 98 | Горизонтальная прокрутка. |
| CircularArrow | 99 | Круговая стрелка. |
| CustomShape | 100 | Этот тип фигуры, по-видимому, предназначен для фигур, которые не входят в стандартный набор автофигур в Microsoft Word. Например, если вы вставляете новую автофигуру из ClipArt. Вы не можете создавать фигуры этого типа в документе. |
| UturnArrow | 101 | Стрелка разворота. |
| CurvedRightArrow | 102 | Изогнутая правая стрелка. |
| CurvedLeftArrow | 103 | Изогнутая левая стрелка. |
| CurvedUpArrow | 104 | Изогнутая стрелка вверх. |
| CurvedDownArrow | 105 | Изогнутая стрелка вниз. |
| CloudCallout | 106 | Облачная выноска. |
| EllipseRibbon | 107 | Эллиптическая лента. |
| EllipseRibbon2 | 108 | Эллиптическая лента 2. |
| FlowChartProcess | 109 | Процесс блок-схемы. |
| FlowChartDecision | 110 | Решение блок-схемы. |
| FlowChartInputOutput | 111 | Ввод-вывод блок-схемы. |
| FlowChartPredefinedProcess | 112 | Предопределённый процесс блок-схемы. |
| FlowChartInternalStorage | 113 | Внутреннее хранилище блок-схемы. |
| FlowChartDocument | 114 | Документ блок-схемы. |
| FlowChartMultidocument | 115 | Мультидокумент блок-схемы. |
| FlowChartTerminator | 116 | Терминатор блок-схемы. |
| FlowChartPreparation | 117 | Подготовка блок-схемы. |
| FlowChartManualInput | 118 | Ручной ввод блок-схемы. |
| FlowChartManualOperation | 119 | Ручная операция блок-схемы. |
| FlowChartConnector | 120 | Соединитель блок-схемы. |
| FlowChartPunchedCard | 121 | Перфокарта блок-схемы. |
| FlowChartPunchedTape | 122 | Перфолента блок-схемы. |
| FlowChartSummingJunction | 123 | Суммирующий узел блок-схемы. |
| FlowChartOr | 124 | Или блок-схемы. |
| FlowChartCollate | 125 | Сборка блок-схемы. |
| FlowChartSort | 126 | Сортировка блок-схемы. |
| FlowChartExtract | 127 | Извлечение блок-схемы. |
| FlowChartMerge | 128 | Объединение блок-схемы. |
| FlowChartOfflineStorage | 129 | Оффлайн-хранение блок-схемы. |
| FlowChartOnlineStorage | 130 | Онлайн-хранение блок-схемы. |
| FlowChartMagneticTape | 131 | Магнитная лента блок-схемы. |
| FlowChartMagneticDisk | 132 | Магнитный диск блок-схемы. |
| FlowChartMagneticDrum | 133 | Магнитный барабан блок-схемы. |
| FlowChartDisplay | 134 | Отображение блок-схемы. |
| FlowChartDelay | 135 | Задержка блок-схемы. |
| TextPlainText | 136 | Простой текст, объект WordArt. |
| TextStop | 137 | Стоп, объект WordArt. |
| TextTriangle | 138 | Треугольник, объект WordArt. |
| TextTriangleInverted | 139 | Треугольник перевёрнутый, объект WordArt. |
| TextChevron | 140 | Шеврон, объект WordArt. |
| TextChevronInverted | 141 | Шеврон перевёрнутый, объект WordArt. |
| TextRingInside | 142 | Кольцо внутри, объект WordArt. |
| TextRingOutside | 143 | Кольцо снаружи, объект WordArt. |
| TextArchUpCurve | 144 | Арка вверх, объект WordArt. |
| TextArchDownCurve | 145 | Арка вниз, объект WordArt. |
| TextCircleCurve | 146 | Кривая круга, объект WordArt. |
| TextButtonCurve | 147 | Кривая кнопки, объект WordArt. |
| TextArchUpPour | 148 | Арка сверху, объект WordArt. |
| TextArchDownPour | 149 | Арка снизу, объект WordArt. |
| TextCirclePour | 150 | Круговой налив, объект WordArt. |
| TextButtonPour | 151 | Кнопка налив, объект WordArt. |
| TextCurveUp | 152 | Изгиб вверх, объект WordArt. |
| TextCurveDown | 153 | Изгиб вниз, объект WordArt. |
| TextCascadeUp | 154 | Каскад вверх, объект WordArt. |
| TextCascadeDown | 155 | Каскад вниз, объект WordArt. |
| TextWave1 | 156 | Волна 1, объект WordArt. |
| TextWave2 | 157 | Волна 2, объект WordArt. |
| TextWave3 | 158 | Волна 3, объект WordArt. |
| TextWave4 | 159 | Волна 4, объект WordArt. |
| TextInflate | 160 | Надуть, объект WordArt. |
| TextDeflate | 161 | Сдуть, объект WordArt. |
| TextInflateBottom | 162 | Надуть снизу, объект WordArt. |
| TextDeflateBottom | 163 | Сжать снизу, объект WordArt. |
| TextInflateTop | 164 | Разжать сверху, объект WordArt. |
| TextDeflateTop | 165 | Сжать сверху, объект WordArt. |
| TextDeflateInflate | 166 | Сжать разжать, объект WordArt. |
| TextDeflateInflateDeflate | 167 | Сжать разжать сжать, объект WordArt. |
| TextFadeRight | 168 | Исчезать вправо, объект WordArt. |
| TextFadeLeft | 169 | Исчезать влево, объект WordArt. |
| TextFadeUp | 170 | Исчезать вверх, объект WordArt. |
| TextFadeDown | 171 | Исчезать вниз, объект WordArt. |
| TextSlantUp | 172 | Наклон вверх, объект WordArt. |
| TextSlantDown | 173 | Наклон вниз, объект WordArt. |
| TextCanUp | 174 | Поднять, объект WordArt. |
| TextCanDown | 175 | Опустить, объект WordArt. |
| FlowChartAlternateProcess | 176 | Альтернативный процесс блок-схемы. |
| FlowChartOffpageConnector | 177 | Соединитель блок-схемы за пределами страницы. |
| Callout90 | 178 | Выноска 90. |
| AccentCallout90 | 179 | Выделенная выноска 90. |
| BorderCallout90 | 180 | [Border](../../aspose.words/border/) выноска 90. |
| AccentBorderCallout90 | 181 | Выделенная граница выноска 90. |
| LeftRightUpArrow | 182 | Стрелка влево-вправо-вверх. |
| Sun | 183 | Солнце. |
| Moon | 184 | Луна. |
| BracketPair | 185 | Пара скобок. |
| BracePair | 186 | Пара фигурных скобок. |
| Seal4 | 187 | Четырехлучевая звезда. |
| ДвойнаяВолна | 188 | Двойная волна. |
| ActionButtonBlank | 189 | Кнопка действия пустая. |
| ActionButtonHome | 190 | Кнопка действия домой. |
| ActionButtonHelp | 191 | Кнопка действия помощи. |
| ActionButtonInformation | 192 | Кнопка действия информации. |
| ActionButtonForwardNext | 193 | Кнопка действия вперёд далее. |
| ActionButtonBackPrevious | 194 | Кнопка действия назад предыдущая. |
| ActionButtonEnd | 195 | Кнопка действия конец. |
| ActionButtonBeginning | 196 | Кнопка действия начало. |
| ActionButtonReturn | 197 | Кнопка действия возврат. |
| ActionButtonDocument | 198 | Кнопка действия документ. |
| ActionButtonSound | 199 | Кнопка действия звук. |
| ActionButtonMovie | 200 | Кнопка действия фильм. |
| SingleCornerSnipped | 203 | Вырезать объект прямоугольника с одним обрезанным углом. |
| TopCornersSnipped | 204 | Вырезать прямоугольник с углом той же стороны. |
| DiagonalCornersSnipped | 205 | Вырезать прямоугольник с диагональным углом. |
| TopCornersOneRoundedOneSnipped | 206 | Вырезать и скруглить прямоугольник с одним углом. |
| SingleCornerRounded | 207 | Скруглить прямоугольник с одним углом. |
| TopCornersRounded | 208 | Скруглить прямоугольник с углом той же стороны. |
| DiagonalCornersRounded | 209 | Скруглить прямоугольник с диагональным углом. |
| Heptagon | 210 | Гептагон. |
| Cloud | 211 | Облако. |
| Seal6 | 212 | Шестиконечная звезда. |
| Seal7 | 213 | Семиконечная звезда. |
| Seal10 | 214 | Десятиконечная звезда. |
| Seal12 | 215 | Двенадцатиконечная звезда. |
| SwooshArrow | 216 | Стрелка‑свисток. |
| Капля | 217 | Капля. |
| КвадратныеВкладки | 218 | Квадратные вкладки. |
| ВкладкиПластин | 219 | Вкладки пластин. |
| Круговая диаграмма | 220 | Круговая диаграмма. |
| СекторныйКруг | 221 | Секторный круг. |
| ОбратнаяЛиния | 222 | Обратная линия. |
| MathPlus | 223 | [Math](../../aspose.words.math/) плюс. |
| MathMinus | 224 | [Math](../../aspose.words.math/) минус. |
| MathMultiply | 225 | [Math](../../aspose.words.math/) умножить. |
| MathDivide | 226 | [Math](../../aspose.words.math/) делить. |
| MathEqual | 227 | [Math](../../aspose.words.math/) равно. |
| MathNotEqual | 228 | [Math](../../aspose.words.math/) не равно. |
| НеравнобедреннаяТрапеция | 229 | Неравнобедренная трапеция. |
| КруговаяСтрелкаВлевоВправо | 230 | Круговая стрелка влево‑вправо. |
| ЛентаВлевоВправо | 231 | Лента влево‑вправо. |
| Стрелка влево по кругу | 232 | Стрелка влево по кругу. |
| Рамка | 233 | Рамка. |
| Полурaмка | 234 | Полурaмка. |
| Воронка | 235 | Воронка. |
| Шестерня6 | 236 | Шестерня с шестью зубьями. |
| Шестерня9 | 237 | Шестерня с девятью зубьями. |
| Десятиугольник | 238 | Десятиугольник. |
| Двенадцатиугольник | 239 | Двенадцатиугольник. |
| Диагональная полоса | 240 | Диагональная полоса. |
| Угол | 241 | Угол. |
| Угловые вкладки | 242 | Угловые вкладки. |
| Хорда | 243 | Хорда. |
| ГрафикПлюс | 244 | Chart plus. |
| ChartStar | 245 | Chart star. |
| ChartX | 246 | Chart X. |
| MinValue | н/д | Зарезервировано для использования системой. |


## Примеры



Показывает, как вставить форму с изображением из локальной файловой системы в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Публичный конструктор класса "Shape" создаст форму с типом разметки "ShapeMarkupLanguage.Vml".
// Если вам нужно создать форму нестандартного типа, например SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded или DiagonalCornersRounded,
// пожалуйста, используйте DocumentBuilder.InsertShape.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Image);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Windows MetaFile.wmf");
shape->set_Width(100);
shape->set_Height(100);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

doc->Save(get_ArtifactsDir() + u"Image.FromFile.docx");
```


Показывает, как Aspose.Words определяет формы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertShape(Aspose::Words::Drawing::ShapeType::Heptagon, Aspose::Words::Drawing::RelativeHorizontalPosition::Page, 0, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 0, 0, 0, Aspose::Words::Drawing::WrapType::None);

builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cloud, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, 0, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 0, 0, 0, Aspose::Words::Drawing::WrapType::None);

builder->InsertShape(Aspose::Words::Drawing::ShapeType::MathPlus, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, 0, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 0, 0, 0, Aspose::Words::Drawing::WrapType::None);

// Чтобы правильно определять типы форм, необходимо работать с формами как DML.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
// "Strict" или "Transitional" совместимость позволяет сохранять форму как DML.
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(get_ArtifactsDir() + u"Shape.ShapeTypes.docx", saveOptions);
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.ShapeTypes.docx");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

for (System::SharedPtr<Aspose::Words::Drawing::Shape> shape : shapes)
{
    std::cout << System::EnumGetName(shape->get_ShapeType()) << std::endl;
}
```

## См. также

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
