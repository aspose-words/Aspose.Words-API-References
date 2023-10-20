---
title: HtmlSaveOptions.FontResourcesSubsettingSizeThreshold
linktitle: FontResourcesSubsettingSizeThreshold
articleTitle: FontResourcesSubsettingSizeThreshold
second_title: Aspose.Words para .NET
description: HtmlSaveOptions FontResourcesSubsettingSizeThreshold propiedad. Controla qué recursos de fuentes necesitan subconjuntos al guardar en HTML MHTML o EPUB. El valor predeterminado es0  en C#.
type: docs
weight: 290
url: /es/net/aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions.FontResourcesSubsettingSizeThreshold property

Controla qué recursos de fuentes necesitan subconjuntos al guardar en HTML, MHTML o EPUB. El valor predeterminado es`0` .

```csharp
public int FontResourcesSubsettingSizeThreshold { get; set; }
```

## Observaciones

[`ExportFontResources`](../exportfontresources/) permite exportar fuentes como archivos subsidiarios o como partes del paquete output . Si el documento utiliza muchas fuentes, especialmente con una gran cantidad de glifos, el tamaño de salida puede crecer significativamente. El subconjunto de fuentes reduce el tamaño del recurso de fuente exportado al filtrar los glifos que no son utilizados por el documento actual.

El subconjunto de fuentes funciona de la siguiente manera:

* De forma predeterminada, todas las fuentes exportadas están subconjuntos.
* Configuración`FontResourcesSubsettingSizeThreshold` un valor positivo indica a Aspose.Words que cree subconjuntos de fuentes cuyo tamaño de archivo sea mayor que el valor especificado.
* Establecer la propiedad enMaxValue suprime el subconjunto de fuentes.

**¡Importante!** Al exportar recursos de fuentes, se deben considerar cuestiones de licencia de fuentes. Los autores que deseen utilizar fuentes específicas a través de un mecanismo de fuente descargable siempre deben verificar cuidadosamente que el uso previsto esté dentro del alcance de la licencia de fuente. Actualmente, muchas fuentes comerciales no permiten la descarga web de sus fuentes en ningún formato. Los acuerdos de licencia que cubren algunas fuentes señalan específicamente que el uso a través de**@Perfil delantero** Rules en hojas de estilo CSS no está permitido. El subconjunto de fuentes también puede violar los términos de la licencia.

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
// Supongamos que configuramos el indicador "ExportFontResources" en "true" y también nombramos una carpeta en la propiedad "FontsFolder".
// En ese caso, la operación de guardar creará esa carpeta y colocará un archivo .ttf dentro
// esa carpeta para cada fuente que utiliza nuestro documento.
// Cada archivo .ttf contendrá el conjunto completo de glifos de esa fuente,
// lo que potencialmente puede resultar en un archivo muy grande que acompaña al documento.
// Cuando aplicamos un subconjunto a una fuente, sus datos sin procesar exportados solo contendrán los glifos que contiene el documento
// usando en lugar de todo el conjunto de glifos. Si el texto de nuestro documento sólo utiliza una pequeña fracción de una fuente
// conjunto de glifos, luego el subconjunto reducirá significativamente el tamaño de nuestros documentos de salida.
// Podemos usar la propiedad "FontResourcesSubsettingSizeThreshold" para definir un tamaño de archivo .ttf, en bytes.
 // Si una fuente exportada crea un archivo de tamaño mayor que ese, entonces la operación de guardar aplicará un subconjunto a esa fuente.
// Establecer un umbral de 0 aplica el subconjunto a todas las fuentes,
// y configurarlo en "int.MaxValue" deshabilita efectivamente el subconjunto.
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
    // De forma predeterminada, los archivos .ttf para cada una de nuestras tres fuentes tendrán más de 700 MB.
    // El subconjunto los reducirá todos a menos de 30 MB.
    FileInfo fontFileInfo = new FileInfo(filename);

    Assert.True(fontFileInfo.Length > 700000 || fontFileInfo.Length < 30000);
    Assert.True(Math.Max(fontResourcesSubsettingSizeThreshold, 30000) > new FileInfo(filename).Length);
}
```

### Ver también

* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
