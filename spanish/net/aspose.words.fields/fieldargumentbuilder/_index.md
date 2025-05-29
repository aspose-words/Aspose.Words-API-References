---
title: FieldArgumentBuilder Class
linktitle: FieldArgumentBuilder
articleTitle: FieldArgumentBuilder
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Fields.FieldArgumentBuilder para crear sin esfuerzo argumentos de campo complejos con nodos y texto para una mejor automatización de documentos.
type: docs
weight: 1960
url: /es/net/aspose.words.fields/fieldargumentbuilder/
---
## FieldArgumentBuilder class

Crea un argumento de campo complejo que consta de campos, nodos y texto sin formato.

Para obtener más información, visite el[Trabajar con campos](https://docs.aspose.com/words/net/working-with-fields/) Artículo de documentación.

```csharp
public class FieldArgumentBuilder
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FieldArgumentBuilder](fieldargumentbuilder/)() | Inicializa una instancia de la`FieldArgumentBuilder` clase. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [AddField](../../aspose.words.fields/fieldargumentbuilder/addfield/)(*[FieldBuilder](../fieldbuilder/)*) | Agrega un campo representado por un[`FieldBuilder`](../fieldbuilder/) al argumento. |
| [AddNode](../../aspose.words.fields/fieldargumentbuilder/addnode/)(*[Inline](../../aspose.words/inline/)*) | Agrega un nodo al argumento. |
| [AddText](../../aspose.words.fields/fieldargumentbuilder/addtext/)(*string*) | Agrega un texto simple al argumento. |

## Ejemplos

Muestra cómo construir campos utilizando un generador de campos y luego insertarlos en el documento.

```csharp
Document doc = new Document();

// A continuación se muestran tres ejemplos de construcción de campos realizados utilizando un generador de campos.
// 1 - Campo único:
// Utilice un generador de campos para agregar un campo SÍMBOLO que muestre el símbolo ƒ (Florín).
FieldBuilder builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(402);
builder.AddSwitch("\\f", "Arial");
builder.AddSwitch("\\s", 25);
builder.AddSwitch("\\u");
Field field = builder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph);

Assert.AreEqual(" SYMBOL 402 \\f Arial \\s 25 \\u ", field.GetFieldCode());

// 2 - Campo anidado:
// Utilice un generador de campos para crear un campo de fórmula utilizado como campo interno por otro generador de campos.
FieldBuilder innerFormulaBuilder = new FieldBuilder(FieldType.FieldFormula);
innerFormulaBuilder.AddArgument(100);
innerFormulaBuilder.AddArgument("+");
innerFormulaBuilder.AddArgument(74);

// Cree otro generador para otro campo SÍMBOLO e inserte el campo de fórmula
 // que hemos creado arriba en el campo SÍMBOLO como su argumento.
builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(innerFormulaBuilder);
field = builder.BuildAndInsert(doc.FirstSection.Body.AppendParagraph(string.Empty));

// El campo SÍMBOLO externo utilizará el resultado del campo de fórmula, 174, como su argumento.
// lo que hará que el campo muestre el símbolo ® (signo registrado) ya que su número de carácter es 174.
Assert.AreEqual(" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field.GetFieldCode());

// 3 - Múltiples campos y argumentos anidados:
// Ahora, usaremos un generador para crear un campo SI, que muestra uno de dos valores de cadena personalizados,
// dependiendo del valor verdadero/falso de su expresión. Para obtener un valor verdadero/falso
// que determina qué cadena muestra el campo SI, el campo SI probará dos expresiones numéricas para determinar su igualdad.
// Proporcionaremos las dos expresiones en forma de campos de fórmula, que anidaremos dentro del campo SI.
FieldBuilder leftExpression = new FieldBuilder(FieldType.FieldFormula);
leftExpression.AddArgument(2);
leftExpression.AddArgument("+");
leftExpression.AddArgument(3);

FieldBuilder rightExpression = new FieldBuilder(FieldType.FieldFormula);
rightExpression.AddArgument(2.5);
rightExpression.AddArgument("*");
rightExpression.AddArgument(5.2);

// A continuación, crearemos dos argumentos de campo, que servirán como cadenas de salida verdaderas/falsas para el campo SI.
// Estos argumentos reutilizarán los valores de salida de nuestras expresiones numéricas.
FieldArgumentBuilder trueOutput = new FieldArgumentBuilder();
trueOutput.AddText("True, both expressions amount to ");
trueOutput.AddField(leftExpression);

FieldArgumentBuilder falseOutput = new FieldArgumentBuilder();
falseOutput.AddNode(new Run(doc, "False, "));
falseOutput.AddField(leftExpression);
falseOutput.AddNode(new Run(doc, " does not equal "));
falseOutput.AddField(rightExpression);

 // Finalmente, crearemos un generador de campos más para el campo SI y combinaremos todas las expresiones.
builder = new FieldBuilder(FieldType.FieldIf);
builder.AddArgument(leftExpression);
builder.AddArgument("=");
builder.AddArgument(rightExpression);
builder.AddArgument(trueOutput);
builder.AddArgument(falseOutput);
field = builder.BuildAndInsert(doc.FirstSection.Body.AppendParagraph(string.Empty));

Assert.AreEqual(" IF \u0013 = 2 + 3 \u0014\u0015 = \u0013 = 2.5 * 5.2 \u0014\u0015 " +
                "\"True, both expressions amount to \u0013 = 2 + 3 \u0014\u0015\" " +
                "\"False, \u0013 = 2 + 3 \u0014\u0015 does not equal \u0013 = 2.5 * 5.2 \u0014\u0015\" ", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SYMBOL.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)
