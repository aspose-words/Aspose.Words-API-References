---
title: "Constructor Aspose::Words::Fields::FieldArgumentBuilder::FieldArgumentBuilder"
linktitle: "FieldArgumentBuilder"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Constructor Aspose::Words::Fields::FieldArgumentBuilder::FieldArgumentBuilder. Inicializa una instancia de la clase FieldArgumentBuilder en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fields/fieldargumentbuilder/fieldargumentbuilder/
---
## FieldArgumentBuilder::FieldArgumentBuilder constructor


Inicializa una instancia de la clase [FieldArgumentBuilder](../).

```cpp
Aspose::Words::Fields::FieldArgumentBuilder::FieldArgumentBuilder()
```


## Ejemplos



Muestra cómo construir campos usando un constructor de campos y luego insertarlos en el documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// A continuación se presentan tres ejemplos de construcción de campos realizados con un constructor de campos.
// 1 -  Campo único:
// Utilice un generador de campos para agregar un campo **SYMBOL** que muestre el símbolo ƒ (Florín).
auto builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(402);
builder->AddSwitch(u"\\f", u"Arial");
builder->AddSwitch(u"\\s", 25);
builder->AddSwitch(u"\\u");
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph());

ASSERT_EQ(u" SYMBOL 402 \\f Arial \\s 25 \\u ", field->GetFieldCode());

// 2 -  Campo anidado:
// Utilice un generador de campos para crear un campo de fórmula que se use como campo interno por otro generador de campos.
auto innerFormulaBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
innerFormulaBuilder->AddArgument(100);
innerFormulaBuilder->AddArgument(u"+");
innerFormulaBuilder->AddArgument(74);

// Cree otro generador para otro campo **SYMBOL** y inserte el campo de fórmula
// que hemos creado arriba en el campo **SYMBOL** como su argumento.
builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(innerFormulaBuilder);
field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->AppendParagraph(System::String::Empty));

// El campo **SYMBOL** externo usará el resultado del campo de fórmula, 174, como su argumento,
// lo que hará que el campo muestre el símbolo ® (Signo de registro) ya que su número de carácter es 174.
ASSERT_EQ(u" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field->GetFieldCode());

// 3 -  Múltiples campos anidados y argumentos:
// Ahora, utilizaremos un generador para crear un campo **IF**, que muestra uno de dos valores de cadena personalizados,
// dependiendo del valor verdadero/falso de su expresión. Para obtener un valor verdadero/falso
// que determina qué cadena muestra el campo **IF**, el campo **IF** probará dos expresiones numéricas para igualdad.
// Proporcionaremos las dos expresiones en forma de campos de fórmula, que anidaremos dentro del campo **IF**.
auto leftExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
leftExpression->AddArgument(2);
leftExpression->AddArgument(u"+");
leftExpression->AddArgument(3);

auto rightExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
rightExpression->AddArgument(2.5);
rightExpression->AddArgument(u"*");
rightExpression->AddArgument(5.2);

// A continuación, construiremos dos argumentos de campo, que servirán como cadenas de salida verdadero/falso para el campo **IF**.
// Estos argumentos reutilizarán los valores de salida de nuestras expresiones numéricas.
auto trueOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
trueOutput->AddText(u"True, both expressions amount to ");
trueOutput->AddField(leftExpression);

auto falseOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u"False, "));
falseOutput->AddField(leftExpression);
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u" does not equal "));
falseOutput->AddField(rightExpression);

// Finalmente, crearemos un generador de campos más para el campo **IF** y combinaremos todas las expresiones.
builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldIf);
builder->AddArgument(leftExpression);
builder->AddArgument(u"=");
builder->AddArgument(rightExpression);
builder->AddArgument(trueOutput);
builder->AddArgument(falseOutput);
field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->AppendParagraph(System::String::Empty));

ASSERT_EQ(System::String(u" IF \u0013 = 2 + 3 \u0014\u0015 = \u0013 = 2.5 * 5.2 \u0014\u0015 ") + u"\"True, both expressions amount to \u0013 = 2 + 3 \u0014\u0015\" " + u"\"False, \u0013 = 2 + 3 \u0014\u0015 does not equal \u0013 = 2.5 * 5.2 \u0014\u0015\" ", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SYMBOL.docx");
```

## Ver también

* Class [FieldArgumentBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
