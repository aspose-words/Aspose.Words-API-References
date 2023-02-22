---
title: OdtSaveOptions.OdtSaveOptions
second_title: Referencia de API de Aspose.Words para .NET
description: OdtSaveOptions constructor. Inicializa una nueva instancia de esta clase que se puede usar para guardar un documento en elOdt formato.
type: docs
weight: 10
url: /es/net/aspose.words.saving/odtsaveoptions/odtsaveoptions/
---
## OdtSaveOptions() {#constructor}

Inicializa una nueva instancia de esta clase que se puede usar para guardar un documento en elOdt formato.

```csharp
public OdtSaveOptions()
```

### Ejemplos

Muestra cómo hacer que un documento guardado se ajuste a un esquema ODT anterior.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Ver también

* class [OdtSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../odtsaveoptions/)
* asamblea [Aspose.Words](../../../)

---

## OdtSaveOptions(string) {#constructor_2}

Inicializa una nueva instancia de esta clase que se puede usar para guardar un documento en elOdt format encriptado con una contraseña.

```csharp
public OdtSaveOptions(string password)
```

### Ver también

* class [OdtSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../odtsaveoptions/)
* asamblea [Aspose.Words](../../../)

---

## OdtSaveOptions(SaveFormat) {#constructor_1}

Inicializa una nueva instancia de esta clase que se puede usar para guardar un documento en elOdt or Ott formato.

```csharp
public OdtSaveOptions(SaveFormat saveFormat)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| saveFormat | SaveFormat | Puede serOdt oOtt. |

### Ejemplos

Muestra cómo cifrar un documento ODT/OTT guardado con una contraseña y luego cargarlo usando Aspose.Words.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Cree un nuevo OdtSaveOptions y pase "SaveFormat.Odt",
// o "SaveFormat.Ott" como formato para guardar el documento. 
OdtSaveOptions saveOptions = new OdtSaveOptions(saveFormat);
saveOptions.Password = "@sposeEncrypted_1145";

string extensionString = FileFormatUtil.SaveFormatToExtension(saveFormat);

// Si abrimos este documento con un editor apropiado,
// nos pedirá la contraseña que especificamos en el objeto SaveOptions.
doc.Save(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString, saveOptions);

FileFormatInfo docInfo = FileFormatUtil.DetectFileFormat(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString);

Assert.IsTrue(docInfo.IsEncrypted);

// Si deseamos abrir o editar este documento nuevamente usando Aspose.Words,
// tendremos que proporcionar un objeto LoadOptions con la contraseña correcta al constructor de carga.
doc = new Document(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString,
    new LoadOptions("@sposeEncrypted_1145"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Ver también

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [OdtSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../odtsaveoptions/)
* asamblea [Aspose.Words](../../../)


