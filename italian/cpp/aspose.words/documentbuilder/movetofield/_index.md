---
title: "Aspose::Words::DocumentBuilder::MoveToField metodo"
linktitle: "MoveToField"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DocumentBuilder::MoveToField metodo. Sposta il cursore su un campo nel documento in C++."
type: docs
weight: 56000
url: /it/cpp/aspose.words/documentbuilder/movetofield/
---
## DocumentBuilder::MoveToField method


Sposta il cursore su un campo nel documento.

```cpp
void Aspose::Words::DocumentBuilder::MoveToField(const System::SharedPtr<Aspose::Words::Fields::Field> &field, bool isAfter)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| campo | const System::SharedPtr\<Aspose::Words::Fields::Field\>\& | Il campo a cui spostare il cursore. |
| isAfter | bool | Quando **true**, sposta il cursore in modo che sia dopo la fine del campo. Quando **false**, sposta il cursore in modo che sia prima dell'inizio del campo. |

## Esempi



Mostra come spostare il cursore del punto di inserimento dei nodi del document builder a un campo specifico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci un campo usando il DocumentBuilder e aggiungi un run di testo dopo di esso.
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u" AUTHOR \"John Doe\" ");

// Il cursore del builder è attualmente alla fine del documento.
ASSERT_TRUE(System::TestTools::IsNull(builder->get_CurrentNode()));

// Sposta il cursore al campo specificando se posizionarlo prima o dopo il campo.
builder->MoveToField(field, moveCursorToAfterTheField);

// Nota che il cursore è al di fuori del campo in entrambi i casi.
// Ciò significa che non possiamo modificare il campo usando il builder in questo modo.
// Per modificare un campo, possiamo usare il metodo MoveTo del builder su un FieldStart di un campo
// o nodo FieldSeparator per posizionare il cursore all'interno.
if (moveCursorToAfterTheField)
{
    ASSERT_TRUE(System::TestTools::IsNull(builder->get_CurrentNode()));
    builder->Write(u" Text immediately after the field.");

    ASSERT_EQ(u"\u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015 Text immediately after the field.", doc->GetText().Trim());
}
else
{
    ASPOSE_ASSERT_EQ(field->get_Start(), builder->get_CurrentNode());
    builder->Write(u"Text immediately before the field. ");

    ASSERT_EQ(u"Text immediately before the field. \u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015", doc->GetText().Trim());
}
```

## Vedi anche

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
