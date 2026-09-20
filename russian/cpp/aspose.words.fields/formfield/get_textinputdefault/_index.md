---
title: "Метод Aspose::Words::Fields::FormField::get_TextInputDefault"
linktitle: "get_TextInputDefault"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::FormField::get_TextInputDefault. Получает или задает строку по умолчанию или выражение расчёта текстового поля формы в C++."
type: docs
weight: 21000
url: /ru/cpp/aspose.words.fields/formfield/get_textinputdefault/
---
## FormField::get_TextInputDefault method


Получает или задает строку по умолчанию или выражение вычисления текстового поля формы.

```cpp
System::String Aspose::Words::Fields::FormField::get_TextInputDefault()
```

## Примечания


Смысл этого свойства зависит от значения свойства [TextInputType](../get_textinputtype/).

Когда [TextInputType](../get_textinputtype/) имеет значение [Regular](../../textformfieldtype/) или [Number](../../textformfieldtype/), эта строка задаёт строку по умолчанию для текстового поля формы. Эта строка является содержимым, которое Microsoft Word будет отображать в документе, когда поле формы пусто.

Когда [TextInputType](../get_textinputtype/) имеет значение [Calculated](../../textformfieldtype/), эта строка содержит выражение для вычисления. Выражение должно быть формулой, действительной в соответствии с требованиями полей формул Microsoft Word. При установке нового выражения через это свойство Aspose.Words автоматически вычисляет результат формулы и вставляет его в поле формы.

Microsoft Word допускает строки длиной не более 255 символов.
## См. также

* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
