---
title: HtmlSaveOptions.FontResourcesSubsettingSizeThreshold
linktitle: FontResourcesSubsettingSizeThreshold
articleTitle: FontResourcesSubsettingSizeThreshold
second_title: Aspose.Words para .NET
description: Optimice sus archivos HTML, MHTML o EPUB con la propiedad FontResourcesSubsettingSizeThreshold, lo que garantiza una gestión eficiente de los recursos de fuentes. Valor predeterminado 0.
type: docs
weight: 290
url: /es/net/aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions.FontResourcesSubsettingSizeThreshold property

Controla qué recursos de fuente necesitan subconjunto al guardar en HTML, MHTML o EPUB. El valor predeterminado es`0` .

```csharp
public int FontResourcesSubsettingSizeThreshold { get; set; }
```

## Observaciones

[`ExportFontResources`](../exportfontresources/) Permite exportar fuentes como archivos secundarios o como partes del paquete output . Si el documento utiliza muchas fuentes, especialmente con un gran número de glifos, el tamaño de salida puede aumentar significativamente. La creación de subconjuntos de fuentes reduce el tamaño del recurso de fuentes exportado al filtrar los glifos que no utiliza el documento actual.

El subconjunto de fuentes funciona de la siguiente manera:

* De forma predeterminada, todas las fuentes exportadas se subdividen.
* Configuración`FontResourcesSubsettingSizeThreshold` para un valor positivo indica a Aspose.Words que cree un subconjunto de fuentes cuyo tamaño de archivo sea mayor que el valor especificado.
* Establecer la propiedad enMaxValue suprime el subconjunto de fuentes.

**¡Importante!**Al exportar recursos de fuentes, se deben considerar las cuestiones de licencias de fuentes. Los autores que deseen usar fuentes específicas mediante un mecanismo de fuentes descargables deben verificar cuidadosamente que el uso previsto esté dentro del alcance de la licencia de la fuente. Actualmente, muchas fuentes comerciales no permiten la descarga web de sus fuentes en ningún formato. Los acuerdos de licencia que cubren algunas fuentes especifican que el uso mediante**@font-face** rules no está permitido en hojas de estilo CSS. La subdivisión de fuentes también puede infringir los términos de la licencia.

## Ejemplos

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

// Cuando guardamos el documento en HTML, podemos pasar un objeto SaveOptions para configurar el subconjunto de fuentes.
// Supongamos que establecemos el indicador "ExportFontResources" en "verdadero" y también nombramos una carpeta en la propiedad "FontsFolder".
// En ese caso, la operación de guardado creará esa carpeta y colocará un archivo .ttf dentro
//esa carpeta para cada fuente que utiliza nuestro documento.
// Cada archivo .ttf contendrá el conjunto de glifos completo de esa fuente,
// lo que potencialmente puede resultar en un archivo muy grande que acompañe al documento.
// Cuando aplicamos subconjuntos a una fuente, sus datos sin procesar exportados solo contendrán los glifos que contiene el documento.
// usando en lugar de todo el conjunto de glifos. Si el texto de nuestro documento solo usa una pequeña fracción de la fuente...
// conjunto de glifos, luego el subconjunto reducirá significativamente el tamaño de nuestros documentos de salida.
// Podemos usar la propiedad "FontResourcesSubsettingSizeThreshold" para definir el tamaño de un archivo .ttf, en bytes.
 // Si una fuente exportada crea un archivo de tamaño mayor que ese, entonces la operación de guardar aplicará el subconjunto a esa fuente.
// Establecer un umbral de 0 aplica el subconjunto a todas las fuentes,
// y configurarlo como "int.MaxValue" deshabilita efectivamente la creación de subconjuntos.
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
    // De forma predeterminada, los archivos .ttf de cada una de nuestras tres fuentes tendrán más de 700 MB.
    // La subdivisión los reducirá todos a menos de 30 MB.
    FileInfo fontFileInfo = new FileInfo(filename);

    Assert.True(fontFileInfo.Length > 700000 || fontFileInfo.Length < 30000);
    Assert.True(Math.Max(fontResourcesSubsettingSizeThreshold, 30000) > new FileInfo(filename).Length);
}
```

### Ver también

* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
