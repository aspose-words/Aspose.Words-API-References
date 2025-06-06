---
title: FieldEQ Class
linktitle: FieldEQ
articleTitle: FieldEQ
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Fields.FieldEQ para una implementación fluida de campos EQ. Mejore la automatización de documentos con potentes funciones y flexibilidad.
type: docs
weight: 2240
url: /es/net/aspose.words.fields/fieldeq/
---
## FieldEQ class

Implementa el campo EQ.

Para obtener más información, visite el[Trabajar con campos](https://docs.aspose.com/words/net/working-with-fields/) Artículo de documentación.

```csharp
public class FieldEQ : Field
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FieldEQ](fieldeq/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtiene el texto que representa el resultado del campo mostrado. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtiene el nodo que representa el final del campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtiene un[`FieldFormat`](../fieldformat/)objeto que proporciona acceso tipificado al formato del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtiene o establece el LCID del campo. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtiene o establece el texto que está entre el separador de campo y el final del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtiene el nodo que representa el separador de campo. Puede ser`nulo` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtiene el nodo que representa el inicio del campo. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtiene el tipo de campo de Microsoft Word. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [AsOfficeMath](../../aspose.words.fields/fieldeq/asofficemath/)() | Devuelve el objeto Office Math correspondiente al campo EQ. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). Se incluyen tanto el código de campo como el resultado de campo de los campos secundarios. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). |
| [Remove](../../aspose.words.fields/field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo padre, devuelve su párrafo padre. Si el campo ya se ha eliminado, devuelve`nulo` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Realiza la desvinculación del campo. |
| [Update](../../aspose.words.fields/field/update/)() | Realiza la actualización del campo. Se lanza una excepción si el campo ya se está actualizando. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Realiza una actualización de campo. Se lanza una excepción si el campo ya se está actualizando. |

## Ejemplos

Muestra cómo reemplazar el campo EQ con Office Math.

```csharp
Document doc = new Document(MyDir + "Field sample - EQ.docx");
FieldEQ fieldEQ = doc.Range.Fields.OfType<FieldEQ>().First();

OfficeMath officeMath = fieldEQ.AsOfficeMath();

fieldEQ.Start.ParentNode.InsertBefore(officeMath, fieldEQ.Start);
fieldEQ.Remove();

doc.Save(ArtifactsDir + "Field.EQAsOfficeMath.docx");
```

Muestra cómo utilizar el campo EQ para mostrar una variedad de ecuaciones matemáticas.

```csharp
public void FieldEQ()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Un campo EQ muestra una ecuación matemática que consta de uno o muchos elementos.
    // Cada elemento toma la siguiente forma: [interruptor][opciones][argumentos].
    // Puede haber un interruptor y varias opciones posibles.
    // Los argumentos son un conjunto de valores separados por comas y encerrados entre llaves.

    // Aquí utilizamos un generador de documentos para insertar un campo EQ, con un interruptor "\f", que corresponde a "Fracción".
    // Pasaremos los valores 1 y 4 como argumentos, y no utilizaremos ninguna opción.
    //Este campo mostrará una fracción con 1 como numerador y 4 como denominador.
    FieldEQ field = InsertFieldEQ(builder, @"\f(1,4)");

    Assert.AreEqual(@" EQ \f(1,4)", field.GetFieldCode());

    // Un campo EQ puede contener múltiples elementos colocados secuencialmente.
    // También podemos anidar elementos unos dentro de otros colocando los elementos internos
    // dentro de los corchetes de argumentos de los elementos externos.
    // Podemos encontrar la lista completa de conmutadores, junto con sus usos aquí:
    // https://blogs.msdn.microsoft.com/murrays/2018/01/23/microsoft-word-eq-field/

     // A continuación se muestran aplicaciones de nueve conmutadores de campo EQ diferentes que podemos usar para crear diferentes tipos de objetos.
    // 1 - Conmutador de matriz "\a", alineado a la izquierda, 2 columnas, 3 puntos de espaciado horizontal y vertical:
    InsertFieldEQ(builder, @"\a \al \co2 \vs3 \hs3(4x,- 4y,-4x,+ y)");

    // 2 - Interruptor de corchete "\b", carácter de corchete "[", para encerrar el contenido entre corchetes:
    // Tenga en cuenta que estamos anidando una matriz dentro de los corchetes, que en conjunto se verá como una matriz en la salida.
    InsertFieldEQ(builder, @"\b \bc\[ (\a \al \co3 \vs3 \hs3(1,0,0,0,1,0,0,0,1))");

    // 3 - Interruptor de desplazamiento "\d", desplazando el texto "B" 30 espacios a la derecha de "A", mostrando el espacio como un subrayado:
    InsertFieldEQ(builder, @"A \d \fo30 \li() B");

    // 4 - Fórmula que consta de múltiples fracciones:
    InsertFieldEQ(builder, @"\f(d,dx)(u + v) = \f(du,dx) + \f(dv,dx)");

    // 5 - Interruptor integral "\i", con un símbolo de suma:
    InsertFieldEQ(builder, @"\i \su(n=1,5,n)");

    // 6 - Cambio de lista "\l":
    InsertFieldEQ(builder, @"\l(1,1,2,3,n,8,13)");

    // 7 - Cambio radical "\r", que muestra una raíz cúbica de x:
    InsertFieldEQ(builder, @"\r (3,x)");

    // 8 - Cambio de subíndice/superíndice "/s", primero como superíndice y luego como subíndice:
    InsertFieldEQ(builder, @"\s \up8(Superscript) Text \s \do8(Subscript)");

    // 9 - Interruptor de caja "\x", con líneas en la parte superior, inferior, izquierda y derecha de la entrada:
    InsertFieldEQ(builder, @"\x \to \bo \le \ri(5)");

    //Algunas combinaciones más complejas.
    InsertFieldEQ(builder, @"\a \ac \vs1 \co1(lim,n→∞) \b (\f(n,n2 + 12) + \f(n,n2 + 22) + ... + \f(n,n2 + n2))");
    InsertFieldEQ(builder, @"\i (,,  \b(\f(x,x2 + 3x + 2))) \s \up10(2)");
    InsertFieldEQ(builder, @"\i \in( tan x, \s \up2(sec x), \b(\r(3) )\s \up4(t) \s \up7(2)  dt)");

    doc.Save(ArtifactsDir + "Field.EQ.docx");
}

/// <summary>
/// Utilice un generador de documentos para insertar un campo EQ, establecer sus argumentos y comenzar un nuevo párrafo.
/// </summary>
private static FieldEQ InsertFieldEQ(DocumentBuilder builder, string args)
{
    FieldEQ field = (FieldEQ)builder.InsertField(FieldType.FieldEquation, true);
    builder.MoveTo(field.Separator);
    builder.Write(args);
    builder.MoveTo(field.Start.ParentNode);

    builder.InsertParagraph();
    return field;
}
```

### Ver también

* class [Field](../field/)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)
