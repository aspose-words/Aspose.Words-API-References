---
title: "Aspose::Words::Layout::RevisionOptions класс"
linktitle: "RevisionOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Layout::RevisionOptions класс. Позволяет контролировать, как исправления документа обрабатываются во время процесса разметки. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.layout/revisionoptions/
---
## RevisionOptions class


Позволяет управлять тем, как обрабатываются ревизии документа во время процесса компоновки. Чтобы узнать больше, посетите статью документации [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/).

```cpp
class RevisionOptions : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_CommentColor](./get_commentcolor/)() const | Позволяет указать цвет, используемый для комментариев. Значение по умолчанию — [Red](../revisioncolor/). |
| [get_DeleteCellColor](./get_deletecellcolor/)() | Позволяет указать цвет, используемый для удалённых ячеек [Deletion](../../aspose.words/revisiontype/). Значение по умолчанию — [Pink](../revisioncolor/). |
| [get_DeletedTextColor](./get_deletedtextcolor/)() | Позволяет указать цвет, используемый для удалённого содержимого [Deletion](../../aspose.words/revisiontype/). Значение по умолчанию — [ByAuthor](../revisioncolor/). |
| [get_DeletedTextEffect](./get_deletedtexteffect/)() | Позволяет указать эффект, применяемый к удалённому содержимому [Deletion](../../aspose.words/revisiontype/). Значение по умолчанию — [StrikeThrough](../revisiontexteffect/) |
| [get_InsertCellColor](./get_insertcellcolor/)() | Позволяет указать цвет, используемый для вставленных ячеек [Insertion](../../aspose.words/revisiontype/). Значение по умолчанию — [Blue](../revisioncolor/). |
| [get_InsertedTextColor](./get_insertedtextcolor/)() | Позволяет указать цвет, используемый для вставленного содержимого [Insertion](../../aspose.words/revisiontype/). Значение по умолчанию — [ByAuthor](../revisioncolor/). |
| [get_InsertedTextEffect](./get_insertedtexteffect/)() | Позволяет указать эффект, применяемый к вставленному содержимому [Insertion](../../aspose.words/revisiontype/). Значение по умолчанию — [Underline](../revisiontexteffect/). |
| [get_MeasurementUnit](./get_measurementunit/)() const | Позволяет указать единицы измерения для комментариев исправлений. Значение по умолчанию — [Centimeters](../../aspose.words/measurementunits/) |
| [get_MovedFromTextColor](./get_movedfromtextcolor/)() | Позволяет указать цвет, используемый для областей, из которых был перемещён контент [Moving](../../aspose.words/revisiontype/). Значение по умолчанию — [ByAuthor](../revisioncolor/). |
| [get_MovedFromTextEffect](./get_movedfromtexteffect/)() | Позволяет указать эффект, применяемый к областям, из которых был перемещён контент [Moving](../../aspose.words/revisiontype/). Значение по умолчанию — [DoubleStrikeThrough](../revisiontexteffect/) |
| [get_MovedToTextColor](./get_movedtotextcolor/)() | Позволяет указать цвет, используемый для областей, в которые был перемещён контент [Moving](../../aspose.words/revisiontype/). Значение по умолчанию — [ByAuthor](../revisioncolor/). |
| [get_MovedToTextEffect](./get_movedtotexteffect/)() | Позволяет указать эффект, применяемый к областям, в которые был перемещён контент [Moving](../../aspose.words/revisiontype/). Значение по умолчанию — [DoubleUnderline](../revisiontexteffect/) |
| [get_RevisedPropertiesColor](./get_revisedpropertiescolor/)() | Позволяет указать цвет, используемый для содержимого с изменениями свойств форматирования [FormatChange](../../aspose.words/revisiontype/) Значение по умолчанию — [NoHighlight](../revisioncolor/). |
| [get_RevisedPropertiesEffect](./get_revisedpropertieseffect/)() | Позволяет указать эффект для областей содержимого с изменениями свойств форматирования [FormatChange](../../aspose.words/revisiontype/) Значение по умолчанию — [None](../revisiontexteffect/) |
| [get_RevisionBarsColor](./get_revisionbarscolor/)() const | Позволяет указать цвет, используемый для боковых панелей, идентифицирующих строки документа, содержащие исправленную информацию. Значение по умолчанию — [Red](../revisioncolor/). |
| [get_RevisionBarsPosition](./get_revisionbarsposition/)() const | Получает или задаёт позицию отрисовки полос исправлений. Значение по умолчанию — [Outside](../../aspose.words.drawing/horizontalalignment/). |
| [get_RevisionBarsWidth](./get_revisionbarswidth/)() const | Получает или задаёт ширину полос исправлений, в пунктах. |
| [get_ShowInBalloons](./get_showinballoons/)() const | Позволяет указать, отображаются ли исправления в облачках. Значение по умолчанию — [None](../showinballoons/). |
| [get_ShowOriginalRevision](./get_showoriginalrevision/)() const | Позволяет указать, следует ли показывать оригинальный текст вместо исправленного. Значение по умолчанию — **false**. |
| [get_ShowRevisionBars](./get_showrevisionbars/)() const | Позволяет указать, следует ли отображать полосы исправлений рядом со строками, содержащими исправленное содержимое. Значение по умолчанию — **true**. |
| [get_ShowRevisionMarks](./get_showrevisionmarks/)() const | Позволяет указать, следует ли помечать текст исправлений специальной разметкой форматирования. Значение по умолчанию — **true**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CommentColor](./set_commentcolor/)(Aspose::Words::Layout::RevisionColor) | Сеттер для [Aspose::Words::Layout::RevisionOptions::get_CommentColor](./get_commentcolor/). |
| [set_DeleteCellColor](./set_deletecellcolor/)(Aspose::Words::Layout::RevisionColor) | Сеттер для [Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor](./get_deletecellcolor/). |
| [set_DeletedTextColor](./set_deletedtextcolor/)(Aspose::Words::Layout::RevisionColor) | Сеттер для [Aspose::Words::Layout::RevisionOptions::get_DeletedTextColor](./get_deletedtextcolor/). |
| [set_DeletedTextEffect](./set_deletedtexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | Сеттер для [Aspose::Words::Layout::RevisionOptions::get_DeletedTextEffect](./get_deletedtexteffect/). |
| [set_InsertCellColor](./set_insertcellcolor/)(Aspose::Words::Layout::RevisionColor) | Сеттер для [Aspose::Words::Layout::RevisionOptions::get_InsertCellColor](./get_insertcellcolor/). |
| [set_InsertedTextColor](./set_insertedtextcolor/)(Aspose::Words::Layout::RevisionColor) | Сеттер для [Aspose::Words::Layout::RevisionOptions::get_InsertedTextColor](./get_insertedtextcolor/). |
| [set_InsertedTextEffect](./set_insertedtexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | Сеттер для [Aspose::Words::Layout::RevisionOptions::get_InsertedTextEffect](./get_insertedtexteffect/). |
| [set_MeasurementUnit](./set_measurementunit/)(Aspose::Words::MeasurementUnits) | Позволяет указать единицы измерения для комментариев исправлений. Значение по умолчанию — [Centimeters](../../aspose.words/measurementunits/) |
| [set_MovedFromTextColor](./set_movedfromtextcolor/)(Aspose::Words::Layout::RevisionColor) | Сеттер для [Aspose::Words::Layout::RevisionOptions::get_MovedFromTextColor](./get_movedfromtextcolor/). |
| [set_MovedFromTextEffect](./set_movedfromtexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | Сеттер для [Aspose::Words::Layout::RevisionOptions::get_MovedFromTextEffect](./get_movedfromtexteffect/). |
| [set_MovedToTextColor](./set_movedtotextcolor/)(Aspose::Words::Layout::RevisionColor) | Сеттер для [Aspose::Words::Layout::RevisionOptions::get_MovedToTextColor](./get_movedtotextcolor/). |
| [set_MovedToTextEffect](./set_movedtotexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | Сеттер для [Aspose::Words::Layout::RevisionOptions::get_MovedToTextEffect](./get_movedtotexteffect/). |
| [set_RevisedPropertiesColor](./set_revisedpropertiescolor/)(Aspose::Words::Layout::RevisionColor) | Сеттер для [Aspose::Words::Layout::RevisionOptions::get_RevisedPropertiesColor](./get_revisedpropertiescolor/). |
| [set_RevisedPropertiesEffect](./set_revisedpropertieseffect/)(Aspose::Words::Layout::RevisionTextEffect) | Сеттер для [Aspose::Words::Layout::RevisionOptions::get_RevisedPropertiesEffect](./get_revisedpropertieseffect/). |
| [set_RevisionBarsColor](./set_revisionbarscolor/)(Aspose::Words::Layout::RevisionColor) | Сеттер для [Aspose::Words::Layout::RevisionOptions::get_RevisionBarsColor](./get_revisionbarscolor/). |
| [set_RevisionBarsPosition](./set_revisionbarsposition/)(Aspose::Words::Drawing::HorizontalAlignment) | Сеттер для [Aspose::Words::Layout::RevisionOptions::get_RevisionBarsPosition](./get_revisionbarsposition/). |
| [set_RevisionBarsWidth](./set_revisionbarswidth/)(float) | Сеттер для [Aspose::Words::Layout::RevisionOptions::get_RevisionBarsWidth](./get_revisionbarswidth/). |
| [set_ShowInBalloons](./set_showinballoons/)(Aspose::Words::Layout::ShowInBalloons) | Сеттер для [Aspose::Words::Layout::RevisionOptions::get_ShowInBalloons](./get_showinballoons/). |
| [set_ShowOriginalRevision](./set_showoriginalrevision/)(bool) | Сеттер для [Aspose::Words::Layout::RevisionOptions::get_ShowOriginalRevision](./get_showoriginalrevision/). |
| [set_ShowRevisionBars](./set_showrevisionbars/)(bool) | Сеттер для [Aspose::Words::Layout::RevisionOptions::get_ShowRevisionBars](./get_showrevisionbars/). |
| [set_ShowRevisionMarks](./set_showrevisionmarks/)(bool) | Сеттер для [Aspose::Words::Layout::RevisionOptions::get_ShowRevisionMarks](./get_showrevisionmarks/). |
| static [Type](./type/)() |  |

## Примеры



Показывает, как изменить внешний вид правок в отрендеренном выходном документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте правку, затем измените цвет всех правок на зелёный.
builder->Writeln(u"This is not a revision.");
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"This is a revision.");
doc->StopTrackRevisions();
builder->Writeln(u"This is not a revision.");

// Удалите полосу, которая появляется слева от каждой исправленной строки.
doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::BrightGreen);
doc->get_LayoutOptions()->get_RevisionOptions()->set_ShowRevisionBars(false);
doc->get_LayoutOptions()->get_RevisionOptions()->set_RevisionBarsPosition(Aspose::Words::Drawing::HorizontalAlignment::Right);

doc->Save(get_ArtifactsDir() + u"Revision.LayoutOptionsRevisions.pdf");
```

## См. также

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
