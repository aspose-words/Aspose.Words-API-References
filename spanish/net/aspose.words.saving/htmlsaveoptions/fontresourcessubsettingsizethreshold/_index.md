---
title: FontResourcesSubsettingSizeThreshold
second_title: Referencia de API de Aspose.Words para .NET
description: Controla qué recursos de fuentes necesitan subconjuntos al guardar en HTML MHTML o EPUB. El valor predeterminado es0 .
type: docs
weight: 300
url: /es/net/aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions.FontResourcesSubsettingSizeThreshold property

Controla qué recursos de fuentes necesitan subconjuntos al guardar en HTML, MHTML o EPUB. El valor predeterminado es`0` .

```csharp
public int FontResourcesSubsettingSizeThreshold { get; set; }
```

### Observaciones

[`ExportFontResources`](../exportfontresources) permite exportar fuentes como archivos auxiliares o como partes del paquete output . Si el documento utiliza muchas fuentes, especialmente con una gran cantidad de glifos, el tamaño de salida puede crecer significativamente. El subconjunto de fuentes reduce el tamaño del recurso de fuente exportado al filtrar los glifos that no se utilizan en el documento actual.

El subconjunto de fuentes funciona de la siguiente manera:

* De forma predeterminada, todas las fuentes exportadas se subdividen.
* Ajuste`FontResourcesSubsettingSizeThreshold` un valor positivo indica a Aspose.Words que subconjunto de fuentes cuyo tamaño de archivo es mayor que el valor especificado.
* Establecer la propiedad enMaxValue suprime el subconjunto de fuentes.

**¡Importante!** Al exportar recursos de fuentes, se deben considerar los problemas de licencia de fuentes. Los autores que deseen utilizar fuentes específicas a través de un mecanismo de fuente downloadable siempre deben verificar cuidadosamente que su uso previsto esté dentro del alcance de la licencia de la fuente. Actualmente, muchas fuentes comerciales no permiten la descarga web de sus fuentes de ninguna forma. Los acuerdos de licencia que cubren algunas fuentes señalan específicamente que el uso a través de **@Perfil delantero** No se permiten las reglas en las hojas de estilo CSS. La creación de subconjuntos de fuentes también puede infringir los términos de la licencia.

### Ejemplos

Muestra cómo trabajar con subconjuntos de fuentes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Times New Roman";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("Hello world!");

// Cuando guardamos el documento en HTML, podemos pasar un subconjunto de fuentes de configuración del objeto SaveOptions.
// Supongamos que establecemos el indicador "ExportFontResources" en "true" y también nombramos una carpeta en la propiedad "FontsFolder".
// En ese caso, la operación de guardado creará esa carpeta y colocará un archivo .ttf dentro
// esa carpeta para cada fuente que usa nuestro documento.
// Cada archivo .ttf contendrá el conjunto completo de glifos de esa fuente,
// lo que potencialmente puede resultar en un archivo muy grande que acompaña al documento.
// Cuando aplicamos subconjuntos a una fuente, sus datos sin procesar exportados solo contendrán los glifos que el documento es
// usando en lugar de todo el conjunto de glifos. Si el texto de nuestro documento solo usa una pequeña fracción de la fuente
// conjunto de glifos, entonces la creación de subconjuntos reducirá significativamente el tamaño de nuestros documentos de salida.
// Podemos usar la propiedad "FontResourcesSubsettingSizeThreshold" para definir un tamaño de archivo .ttf, en bytes.
  // Si una fuente exportada crea un archivo de tamaño mayor que ese, la operación de guardar aplicará subconjuntos a esa fuente.
// Establecer un umbral de 0 aplica subconjuntos a todas las fuentes,
// y establecerlo en "int.MaxValue" deshabilita efectivamente la creación de subconjuntos.
string fontsFolder = ArtifactsDir + "HtmlSaveOptions.FontSubsetting.Fonts";

HtmlSaveOptions options = new HtmlSaveOptions
{
    ExportFontResources = true,
    FontsFolder = fontsFolder,
    FontResourcesSubsettingSizeThreshold = fontResourcesSubsettingSizeThreshold
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FontSubsetting.html", options);

string[] fontFileNames = Directory.GetFiles(fontsFolder).Where(s => s.EndsWith(".ttf")).ToArray();

Assert.AreEqual(3, fontFileNames.Length);

foreach (string filename in fontFileNames)
{
    // De manera predeterminada, los archivos .ttf para cada una de nuestras tres fuentes tendrán más de 700 MB.
    // La creación de subconjuntos los reducirá a menos de 30 MB.
    FileInfo fontFileInfo = new FileInfo(filename);

    Assert.True(fontFileInfo.Length > 700000 || fontFileInfo.Length < 30000);
    Assert.True(Math.Max(fontResourcesSubsettingSizeThreshold, 30000) > new FileInfo(filename).Length);
}
```

### Ver también

* class [HtmlSaveOptions](../../htmlsaveoptions)
* espacio de nombres [Aspose.Words.Saving](../../htmlsaveoptions)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
