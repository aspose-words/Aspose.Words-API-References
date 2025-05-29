---
title: FieldOptions.IsBidiTextSupportedOnUpdate
linktitle: IsBidiTextSupportedOnUpdate
articleTitle: IsBidiTextSupportedOnUpdate
second_title: Aspose.Words para .NET
description: Descubra si la compatibilidad con texto bidireccional está habilitada en FieldOptions. Gestione fácilmente las actualizaciones de texto para una funcionalidad multilingüe mejorada.
type: docs
weight: 150
url: /es/net/aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/
---
## FieldOptions.IsBidiTextSupportedOnUpdate property

Obtiene o establece el valor que indica si el texto bidireccional es totalmente compatible durante la actualización del campo o no.

```csharp
public bool IsBidiTextSupportedOnUpdate { get; set; }
```

## Observaciones

Cuando esta propiedad se establece en`verdadero`Se realizan pasos adicionales para producir un resultado de campo compatible con language de derecha a izquierda (es decir, árabe o hebreo) durante su actualización.

Cuando esta propiedad se establece en`FALSO` y se utiliza lenguaje de derecha a izquierda, no se garantiza la exactitud del campo result luego de su actualización.

El valor predeterminado es`FALSO`.

## Ejemplos

Muestra cómo utilizar FieldOptions para garantizar que la actualización de campos admita totalmente texto bidireccional.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // Asegúrese de que cualquier operación de campo que involucre texto de derecha a izquierda se realice como se espera.
doc.FieldOptions.IsBidiTextSupportedOnUpdate = true;

// Utilice un generador de documentos para insertar un campo que contenga el texto de derecha a izquierda.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "עֶשְׂרִים", "שְׁלוֹשִׁים", "אַרְבָּעִים", "חֲמִשִּׁים", "שִׁשִּׁים" }, 0);
comboBox.CalculateOnExit = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.Bidi.docx");
```

### Ver también

* class [FieldOptions](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
