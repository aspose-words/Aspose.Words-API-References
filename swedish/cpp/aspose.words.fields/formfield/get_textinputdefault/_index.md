---
title: "Aspose::Words::Fields::FormField::get_TextInputDefault metod"
linktitle: "get_TextInputDefault"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FormField::get_TextInputDefault metod. Hämtar eller anger standardsträngen eller ett beräkningsuttryck för ett textformulärfält i C++."
type: docs
weight: 21000
url: /sv/cpp/aspose.words.fields/formfield/get_textinputdefault/
---
## FormField::get_TextInputDefault method


Hämtar eller anger standardsträngen eller ett beräkningsuttryck för ett textformulärfält.

```cpp
System::String Aspose::Words::Fields::FormField::get_TextInputDefault()
```

## Anmärkningar


Betydelsen av den här egenskapen beror på värdet av egenskapen [TextInputType](../get_textinputtype/).

När [TextInputType](../get_textinputtype/) är [Regular](../../textformfieldtype/) eller [Number](../../textformfieldtype/), anger den här strängen standardsträngen för textformulärfältet. Denna sträng är innehållet som Microsoft Word visar i dokumentet när formulärfältet är tomt.

När [TextInputType](../get_textinputtype/) är [Calculated](../../textformfieldtype/), innehåller den här strängen uttrycket som ska beräknas. Uttrycket måste vara en formel som är giltig enligt Microsoft Words krav för formelfält. När du anger ett nytt uttryck med hjälp av den här egenskapen beräknar Aspose.Words formelresultatet automatiskt och infogar det i formulärfältet.

Microsoft Word tillåter strängar med högst 255 tecken.
## Se även

* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
