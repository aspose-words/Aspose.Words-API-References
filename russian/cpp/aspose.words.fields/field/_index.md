---
title: "Aspose::Words::Fields::Field class"
linktitle: "Поле"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::Field class. Представляет поле документа Microsoft Word. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.fields/field/
---
## Field class


Представляет поле документа Microsoft Word. Чтобы узнать больше, посетите статью документации.

```cpp
class Field : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_DisplayResult](./get_displayresult/)() | Получает текст, представляющий отображаемый результат поля. |
| [get_End](./get_end/)() const | Получает узел, представляющий конец поля. |
| [get_FieldEnd](./get_fieldend/)() const | Получает узел, представляющий конец поля. |
| [get_FieldStart](./get_fieldstart/)() const | Получает узел, представляющий начало поля. |
| [get_Format](./get_format/)() | Получает объект [FieldFormat](../fieldformat/), который предоставляет типизированный доступ к форматированию поля. |
| [get_IsDirty](./get_isdirty/)() | Получает или задает, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ. |
| [get_IsLocked](./get_islocked/)() | Получает или задает, заблокировано ли поле (не должно пересчитывать свой результат). |
| [get_LocaleId](./get_localeid/)() | Получает или задает LCID поля. |
| [get_Result](./get_result/)() | Получает или задает текст, находящийся между разделителем поля и его концом. |
| [get_Separator](./get_separator/)() | Получает узел, представляющий разделитель поля. Может быть **null**. |
| [get_Start](./get_start/)() const | Получает узел, представляющий начало поля. |
| virtual [get_Type](./get_type/)() const | Получает тип поля Microsoft Word. |
| [GetFieldCode](./getfieldcode/)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). Включены как код поля, так и результат дочерних полей. |
| [GetFieldCode](./getfieldcode/)(bool) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](./remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним элементом его родительского узла, возвращает родительский абзац. Если поле уже удалено, возвращает **null**. |
| [set_IsDirty](./set_isdirty/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsDirty](./get_isdirty/). |
| [set_IsLocked](./set_islocked/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsLocked](./get_islocked/). |
| [set_LocaleId](./set_localeid/)(int32_t) | Сеттер для [Aspose::Words::Fields::Field::get_LocaleId](./get_localeid/). |
| [set_Result](./set_result/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::Field::get_Result](./get_result/). |
| static [Type](./type/)() |  |
| [Unlink](./unlink/)() | Выполняет отсоединение поля. |
| [Update](./update/)() | Выполняет обновление поля. Вызывает исключение, если поле уже обновляется. |
| [Update](./update/)(bool) | Выполняет обновление поля. Выбрасывает исключение, если поле уже обновляется. |
## Примечания


Поле в документе Word — это сложная структура, состоящая из нескольких узлов, включающих начало поля, код поля, разделитель поля, результат поля и конец поля. [Fields](../) могут быть вложенными, содержать богатый контент и охватывать несколько абзацев или разделов в документе. Класс [Field](./) является объектом‑\"фасадом\", предоставляющим свойства и методы, позволяющие работать с полем как с единым объектом.

Свойства [Start](./get_start/), [Separator](./get_separator/) и [End](./get_end/) указывают соответственно на узлы начала, разделителя и конца поля.

Содержание между началом поля и разделителем является кодом поля. Содержание между разделителем поля и концом поля является результатом поля. Код поля обычно состоит из одного или нескольких объектов [Run](../../aspose.words/run/), задающих инструкции. Ожидается, что обрабатывающее приложение выполнит код поля для вычисления результата.

Процесс вычисления результатов полей называется обновлением полей. Aspose.Words может обновлять результаты полей большинства типов полей точно так же, как это делает Microsoft Word. Особенно важно, что Aspose.Words может вычислять результаты даже самых сложных формульных полей. Чтобы вычислить результат отдельного поля, используйте метод [Update](./update/). Чтобы обновить поля во всём документе, используйте [UpdateFields](../../aspose.words/document/updatefields/).

Вы можете получить текстовую версию кода поля, используя метод [GetFieldCode()](./getfieldcode/). Вы можете получить и установить текстовую версию результата поля, используя свойство [Result](./get_result/). Как код поля, так и результат могут содержать сложный контент, такой как вложенные поля, абзацы, фигуры, таблицы, и в этом случае вы можете захотеть работать напрямую с узлами поля, если требуется больший контроль.

Вы не создаёте экземпляры класса [Field](./) напрямую. Чтобы создать новое поле, используйте метод [InsertField()](../).

## Примеры



Показывает, как вставить поле в документ, используя код поля.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// Эта перегрузка метода InsertField автоматически обновляет вставленные поля.
ASSERT_TRUE((System::DateTime::get_Today() - System::DateTime::Parse(field->get_Result())).get_Days() <= 1);
```

## См. также

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
