---
title: FieldBuilder.BuildAndInsert
linktitle: BuildAndInsert
articleTitle: BuildAndInsert
second_title: Aspose.Words para .NET
description: FieldBuilder BuildAndInsert método. Crea e inserta un campo en el documento antes del nodo en línea especificado en C#.
type: docs
weight: 40
url: /es/net/aspose.words.fields/fieldbuilder/buildandinsert/
---
## BuildAndInsert(*[Inline](../../../aspose.words/inline/)*) {#buildandinsert}

Crea e inserta un campo en el documento antes del nodo en línea especificado.

```csharp
public Field BuildAndInsert(Inline refNode)
```

### Valor_devuelto

A[`Field`](../../field/) objeto que representa el campo insertado.

## Ejemplos

Muestra cómo crear e insertar un campo usando un generador de campos.

```csharp
Document doc = new Document();

// Una forma conveniente de agregar contenido de texto a un documento es con un generador de documentos.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write(" Hello world! This text is one Run, which is an inline node.");

// Los campos tienen su constructor, que podemos usar para construir un código de campo pieza por pieza.
// En este caso, construiremos un campo CÓDIGO DE BARRAS que representa un código postal de EE. UU.,
// y luego insértelo delante de Run.
FieldBuilder fieldBuilder = new FieldBuilder(FieldType.FieldBarcode);
fieldBuilder.AddArgument("90210");
fieldBuilder.AddSwitch("\\f", "A");
fieldBuilder.AddSwitch("\\u");

fieldBuilder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph.Runs[0]);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CreateWithFieldBuilder.docx");
```

### Ver también

* class [Field](../../field/)
* class [Inline](../../../aspose.words/inline/)
* class [FieldBuilder](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)

---

## BuildAndInsert(*[Paragraph](../../../aspose.words/paragraph/)*) {#buildandinsert_1}

Crea e inserta un campo en el documento hasta el final del párrafo especificado.

```csharp
public Field BuildAndInsert(Paragraph refNode)
```

### Valor_devuelto

A[`Field`](../../field/) objeto que representa el campo insertado.

## Ejemplos

Muestra cómo construir campos usando un generador de campos y luego insertarlos en el documento.

```csharp
Document doc = new Document();

// A continuación se muestran tres ejemplos de construcción de campos realizada utilizando un generador de campos.
// 1 - Campo único:
// Utilice un generador de campos para agregar un campo SÍMBOLO que muestre el símbolo ƒ (Florín).
FieldBuilder builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(402);
builder.AddSwitch("\\f", "Arial");
builder.AddSwitch("\\s", 25);
builder.AddSwitch("\\u");
Field field = builder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph);

Assert.AreEqual(" SYMBOL 402 \\f Arial \\s 25 \\u ", field.GetFieldCode());

// 2 - campo anidado:
// Utilice un generador de campos para crear un campo de fórmula utilizado como campo interno por otro generador de campos.
FieldBuilder innerFormulaBuilder = new FieldBuilder(FieldType.FieldFormula);
innerFormulaBuilder.AddArgument(100);
innerFormulaBuilder.AddArgument("+");
innerFormulaBuilder.AddArgument(74);

// Crea otro constructor para otro campo SÍMBOLO e inserta el campo de fórmula
 // que hemos creado arriba en el campo SÍMBOLO como argumento.
builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(innerFormulaBuilder);
field = builder.BuildAndInsert(doc.FirstSection.Body.AppendParagraph(string.Empty));

// El campo SÍMBOLO externo utilizará el resultado del campo de fórmula, 174, como argumento,
// lo que hará que el campo muestre el símbolo ® (Signo Registrado) ya que su número de carácter es 174.
Assert.AreEqual(" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field.GetFieldCode());

// 3 - Múltiples campos y argumentos anidados:
// Ahora usaremos un constructor para crear un campo IF, que muestra uno de dos valores de cadena personalizados,
// dependiendo del valor verdadero/falso de su expresión. Para obtener un valor verdadero/falso
// que determina qué cadena muestra el campo IF, el campo IF probará la igualdad de dos expresiones numéricas.
// Proporcionaremos las dos expresiones en forma de campos de fórmula, que anidaremos dentro del campo IF.
FieldBuilder leftExpression = new FieldBuilder(FieldType.FieldFormula);
leftExpression.AddArgument(2);
leftExpression.AddArgument("+");
leftExpression.AddArgument(3);

FieldBuilder rightExpression = new FieldBuilder(FieldType.FieldFormula);
rightExpression.AddArgument(2.5);
rightExpression.AddArgument("*");
rightExpression.AddArgument(5.2);

// A continuación, crearemos dos argumentos de campo, que servirán como cadenas de salida de verdadero/falso para el campo IF.
// Estos argumentos reutilizarán los valores de salida de nuestras expresiones numéricas.
FieldArgumentBuilder trueOutput = new FieldArgumentBuilder();
trueOutput.AddText("True, both expressions amount to ");
trueOutput.AddField(leftExpression);

FieldArgumentBuilder falseOutput = new FieldArgumentBuilder();
falseOutput.AddNode(new Run(doc, "False, "));
falseOutput.AddField(leftExpression);
falseOutput.AddNode(new Run(doc, " does not equal "));
falseOutput.AddField(rightExpression);

 // Finalmente, crearemos un generador de campos más para el campo IF y combinaremos todas las expresiones.
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

* class [Field](../../field/)
* class [Paragraph](../../../aspose.words/paragraph/)
* class [FieldBuilder](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
