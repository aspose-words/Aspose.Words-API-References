---
title: FormFieldCollection Class
linktitle: FormFieldCollection
articleTitle: FormFieldCollection
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Fields.FormFieldCollection, su solución ideal para administrar todos los campos de formulario en un documento con facilidad y eficiencia.
type: docs
weight: 3040
url: /es/net/aspose.words.fields/formfieldcollection/
---
## FormFieldCollection class

Una colección de[`FormField`](../formfield/) objetos que representan todos los campos de formulario en un rango.

Para obtener más información, visite el[Trabajar con campos de formulario](https://docs.aspose.com/words/net/working-with-form-fields/) Artículo de documentación.

```csharp
public class FormFieldCollection : IEnumerable<FormField>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words.fields/formfieldcollection/count/) { get; } | Devuelve el número de campos de formulario en la colección. |
| [Item](../../aspose.words.fields/formfieldcollection/item/) { get; } | Devuelve un campo de formulario en el índice especificado. (2 indexers) |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Clear](../../aspose.words.fields/formfieldcollection/clear/)() | Elimina todos los campos de formulario de esta colección y del documento. |
| [GetEnumerator](../../aspose.words.fields/formfieldcollection/getenumerator/)() | Devuelve un objeto enumerador. |
| [Remove](../../aspose.words.fields/formfieldcollection/remove/)(*string*) | Elimina un campo de formulario con el nombre especificado. |
| [RemoveAt](../../aspose.words.fields/formfieldcollection/removeat/)(*int*) | Elimina un campo de formulario en el índice especificado. |

## Ejemplos

Muestra cómo insertar distintos tipos de campos de formulario en un documento y procesarlos mediante una implementación de visitante de documentos.

```csharp
public void Visitor()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Utilice un generador de documentos para insertar un cuadro combinado.
    builder.Write("Choose a value from this combo box: ");
    FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "One", "Two", "Three" }, 0);
    comboBox.CalculateOnExit = true;
    Assert.AreEqual(3, comboBox.DropDownItems.Count);
    Assert.AreEqual(0, comboBox.DropDownSelectedIndex);
    Assert.True(comboBox.Enabled);

    builder.InsertBreak(BreakType.ParagraphBreak);

    // Utilice un generador de documentos para insertar una casilla de verificación.
    builder.Write("Click this check box to tick/untick it: ");
    FormField checkBox = builder.InsertCheckBox("MyCheckBox", false, 50);
    checkBox.IsCheckBoxExactSize = true;
    checkBox.HelpText = "Right click to check this box";
    checkBox.OwnHelp = true;
    checkBox.StatusText = "Checkbox status text";
    checkBox.OwnStatus = true;
    Assert.AreEqual(50.0d, checkBox.CheckBoxSize);
    Assert.False(checkBox.Checked);
    Assert.False(checkBox.Default);

    builder.InsertBreak(BreakType.ParagraphBreak);

    // Utilice un generador de documentos para insertar un campo de formulario de entrada de texto.
    builder.Write("Enter text here: ");
    FormField textInput = builder.InsertTextInput("MyTextInput", TextFormFieldType.Regular, "", "Placeholder text", 50);
    textInput.EntryMacro = "EntryMacro";
    textInput.ExitMacro = "ExitMacro";
    textInput.TextInputDefault = "Regular";
    textInput.TextInputFormat = "FIRST CAPITAL";
    textInput.SetTextInputValue("New placeholder text");
    Assert.AreEqual(TextFormFieldType.Regular, textInput.TextInputType);
    Assert.AreEqual(50, textInput.MaxLength);

    //Esta colección contiene todos nuestros campos de formulario.
    FormFieldCollection formFields = doc.Range.FormFields;
    Assert.AreEqual(3, formFields.Count);

    // Campos muestra los campos de nuestro formulario. Podemos ver sus códigos de campo abriendo este documento.
    // en Microsoft y presionando Alt + F9. Estos campos no tienen modificadores.
    // y los miembros del objeto FormField gobiernan completamente el contenido de sus campos de formulario.
    Assert.AreEqual(3, doc.Range.Fields.Count);
    Assert.AreEqual(" FORMDROPDOWN \u0001", doc.Range.Fields[0].GetFieldCode());
    Assert.AreEqual(" FORMCHECKBOX \u0001", doc.Range.Fields[1].GetFieldCode());
    Assert.AreEqual(" FORMTEXT \u0001", doc.Range.Fields[2].GetFieldCode());

    // Permitir que cada campo de formulario acepte un visitante del documento.
    FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

    using (IEnumerator<FormField> fieldEnumerator = formFields.GetEnumerator())
        while (fieldEnumerator.MoveNext())
            fieldEnumerator.Current.Accept(formFieldVisitor);

    Console.WriteLine(formFieldVisitor.GetText());

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "FormFields.Visitor.html");
}

/// <summary>
 /// Implementación de visitante que imprime detalles de los campos de formulario que visita.
/// </summary>
public class FormFieldVisitor : DocumentVisitor
{
    public FormFieldVisitor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Se llama cuando se encuentra un nodo FormField en el documento.
    /// </summary>
    public override VisitorAction VisitFormField(FormField formField)
    {
        AppendLine(formField.Type + ": \"" + formField.Name + "\"");
        AppendLine("\tStatus: " + (formField.Enabled ? "Enabled" : "Disabled"));
        AppendLine("\tHelp Text:  " + formField.HelpText);
        AppendLine("\tEntry macro name: " + formField.EntryMacro);
        AppendLine("\tExit macro name: " + formField.ExitMacro);

        switch (formField.Type)
        {
            case FieldType.FieldFormDropDown:
                AppendLine("\tDrop-down items count: " + formField.DropDownItems.Count + ", default selected item index: " + formField.DropDownSelectedIndex);
                AppendLine("\tDrop-down items: " + string.Join(", ", formField.DropDownItems.ToArray()));
                break;
            case FieldType.FieldFormCheckBox:
                AppendLine("\tCheckbox size: " + formField.CheckBoxSize);
                AppendLine("\t" + "Checkbox is currently: " + (formField.Checked ? "checked, " : "unchecked, ") + "by default: " + (formField.Default ? "checked" : "unchecked"));
                break;
            case FieldType.FieldFormTextInput:
                AppendLine("\tInput format: " + formField.TextInputFormat);
                AppendLine("\tCurrent contents: " + formField.Result);
                break;
        }

        //Deja que el visitante continúe visitando otros nodos.
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Agrega texto terminado en carácter de nueva línea a la salida actual.
    /// </summary>
    private void AppendLine(string text)
    {
        mBuilder.Append(text + '\n');
    }

    /// <summary>
    /// Obtiene el texto simple del documento que fue acumulado por el visitante.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    private readonly StringBuilder mBuilder;
}
```

### Ver también

* class [FormField](../formfield/)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)
