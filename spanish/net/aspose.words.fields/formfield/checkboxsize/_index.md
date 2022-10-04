---
title: CheckBoxSize
second_title: Referencia de API de Aspose.Words para .NET
description: Obtiene o establece el tamaño de la casilla de verificación en puntos. Sólo tiene efecto cuandoIsCheckBoxExactSizeaspose.words.fields/formfield/ischeckboxexactsize/ es cierto.
type: docs
weight: 20
url: /es/net/aspose.words.fields/formfield/checkboxsize/
---
## FormField.CheckBoxSize property

Obtiene o establece el tamaño de la casilla de verificación en puntos. Sólo tiene efecto cuando[`IsCheckBoxExactSize`](../ischeckboxexactsize/) es cierto.

```csharp
public double CheckBoxSize { get; set; }
```

### Observaciones

Aplicable solo para un campo de formulario de casilla de verificación.

### Ejemplos

Muestra cómo insertar diferentes tipos de campos de formulario en un documento y procesarlos con una implementación de visitante de documentos.

```csharp
public void Visitor()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Use un generador de documentos para insertar un cuadro combinado.
    builder.Write("Choose a value from this combo box: ");
    FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "One", "Two", "Three" }, 0);
    comboBox.CalculateOnExit = true;
    Assert.AreEqual(3, comboBox.DropDownItems.Count);
    Assert.AreEqual(0, comboBox.DropDownSelectedIndex);
    Assert.True(comboBox.Enabled);

    builder.InsertBreak(BreakType.ParagraphBreak);

    // Use un generador de documentos para insertar una casilla de verificación.
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

    // Use un generador de documentos para insertar un campo de formulario de entrada de texto.
    builder.Write("Enter text here: ");
    FormField textInput = builder.InsertTextInput("MyTextInput", TextFormFieldType.Regular, "", "Placeholder text", 50);
    textInput.EntryMacro = "EntryMacro";
    textInput.ExitMacro = "ExitMacro";
    textInput.TextInputDefault = "Regular";
    textInput.TextInputFormat = "FIRST CAPITAL";
    textInput.SetTextInputValue("New placeholder text");
    Assert.AreEqual(TextFormFieldType.Regular, textInput.TextInputType);
    Assert.AreEqual(50, textInput.MaxLength);

    // Esta colección contiene todos nuestros campos de formulario.
    FormFieldCollection formFields = doc.Range.FormFields;
    Assert.AreEqual(3, formFields.Count);

    // Los campos muestran nuestros campos de formulario. Podemos ver sus códigos de campo abriendo este documento
    // en Microsoft y presionando Alt + F9. Estos campos no tienen interruptores,
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
    /// Llamado cuando se encuentra un nodo FormField en el documento.
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

        // Permitir que el visitante continúe visitando otros nodos.
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Agrega texto terminado en caracteres de nueva línea a la salida actual.
    /// </summary>
    private void AppendLine(string text)
    {
        mBuilder.Append(text + '\n');
    }

    /// <summary>
    /// Obtiene el texto sin formato del documento que fue acumulado por el visitante.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    private readonly StringBuilder mBuilder;
}
```

### Ver también

* class [FormField](../)
* espacio de nombres [Aspose.Words.Fields](../../formfield/)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
