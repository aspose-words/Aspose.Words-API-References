---
title: "Méthode Aspose::Words::DocumentBuilder::MoveToField"
linktitle: "MoveToField"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::DocumentBuilder::MoveToField. Déplace le curseur vers un champ dans le document en C++."
type: docs
weight: 56000
url: /fr/cpp/aspose.words/documentbuilder/movetofield/
---
## DocumentBuilder::MoveToField method


Déplace le curseur vers un champ dans le document.

```cpp
void Aspose::Words::DocumentBuilder::MoveToField(const System::SharedPtr<Aspose::Words::Fields::Field> &field, bool isAfter)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| champ | const System::SharedPtr\<Aspose::Words::Fields::Field\>\& | Le champ vers lequel déplacer le curseur. |
| isAfter | bool | Lorsque **true**, déplace le curseur pour qu'il soit après la fin du champ. Lorsque **false**, déplace le curseur pour qu'il soit avant le début du champ. |

## Exemples



Montre comment déplacer le curseur du point d'insertion de nœud du DocumentBuilder vers un champ spécifique.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez un champ à l'aide du DocumentBuilder et ajoutez un segment de texte après celui-ci.
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u" AUTHOR \"John Doe\" ");

// Le curseur du DocumentBuilder est actuellement à la fin du document.
ASSERT_TRUE(System::TestTools::IsNull(builder->get_CurrentNode()));

// Déplacez le curseur vers le champ en précisant s'il faut placer ce curseur avant ou après le champ.
builder->MoveToField(field, moveCursorToAfterTheField);

// Notez que le curseur se trouve à l'extérieur du champ dans les deux cas.
// Cela signifie que nous ne pouvons pas modifier le champ en utilisant le builder de cette manière.
// Pour modifier un champ, nous pouvons utiliser la méthode MoveTo du builder sur le FieldStart d'un champ
// ou le nœud FieldSeparator pour placer le curseur à l'intérieur.
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

## Voir aussi

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
