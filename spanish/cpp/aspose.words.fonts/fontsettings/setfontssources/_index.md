---
title: "Aspose::Words::Fonts::FontSettings::SetFontsSources method"
linktitle: "SetFontsSources"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fonts::FontSettings::SetFontsSources method. Establece las fuentes donde Aspose.Words busca fuentes TrueType al renderizar documentos o incrustar fuentes en C++."
type: docs
weight: 13000
url: /es/cpp/aspose.words.fonts/fontsettings/setfontssources/
---
## FontSettings::SetFontsSources(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\&) method


Establece las fuentes donde Aspose.Words busca fuentes TrueType al renderizar documentos o incrustar fuentes.

```cpp
void Aspose::Words::Fonts::FontSettings::SetFontsSources(const System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> &sources)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sources | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\& | Una matriz de fuentes que contienen fuentes TrueType. |
## Observaciones


Por defecto, Aspose.Words busca fuentes instaladas en el sistema.

Establecer esta propiedad restablece la caché de todas las fuentes cargadas previamente.

## Ejemplos



Mostrar cómo agregar una fuente de fuentes a nuestras fuentes de origen existentes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Amethysta");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");
builder->get_Font()->set_Name(u"Junction Light");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> originalFontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_EQ(1, originalFontSources->get_Length());

ASSERT_TRUE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));

// La fuente de origen predeterminada no incluye dos de las fuentes que estamos usando en nuestro documento.
// Al guardar este documento, Aspose.Words aplicará fuentes de respaldo a todo el texto formateado con fuentes inaccesibles.
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Junction Light";
}))));

// Crear una fuente de origen a partir de una carpeta que contiene fuentes.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), true);

// Aplica una nueva matriz de fuentes que contiene las fuentes originales, así como nuestras fuentes personalizadas.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> updatedFontSources = System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({originalFontSources[0], folderFontSource});
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsSources(updatedFontSources);

// Verifica que Aspose.Words tenga acceso a todas las fuentes requeridas antes de renderizar el documento a PDF.
updatedFontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_TRUE(updatedFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));
ASSERT_TRUE(updatedFontSources[1]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));
ASSERT_TRUE(updatedFontSources[1]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Junction Light";
}))));

doc->Save(get_ArtifactsDir() + u"FontSettings.AddFontSource.pdf");

// Restaurar las fuentes de origen originales.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsSources(originalFontSources);
```

## Ver también

* Class [FontSourceBase](../../fontsourcebase/)
* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FontSettings::SetFontsSources(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\&, const System::SharedPtr\<System::IO::Stream\>\&) method


Establece las fuentes donde Aspose.Words busca fuentes TrueType y, adicionalmente, carga la caché de búsqueda de fuentes guardada previamente.

```cpp
void Aspose::Words::Fonts::FontSettings::SetFontsSources(const System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> &sources, const System::SharedPtr<System::IO::Stream> &cacheInputStream)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sources | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\& | Una matriz de fuentes que contienen fuentes TrueType. |
| cacheInputStream | const System::SharedPtr\<System::IO::Stream\>\& | Secuencia de entrada con caché de búsqueda de fuentes guardada. |
## Observaciones


[Loading](../../../aspose.words.loading/) previously saved font search cache will speed up the font cache initialization process. It is especially useful when access to font sources is complicated (e.g. when fonts are loaded via network).

Al guardar y cargar la caché de búsqueda de fuentes, las fuentes en los orígenes proporcionados se identifican mediante la clave de caché. Para las fuentes en [SystemFontSource](../../systemfontsource/) y [FolderFontSource](../../folderfontsource/) la clave de caché es la ruta al archivo de fuente. Para [MemoryFontSource](../../memoryfontsource/) y [StreamFontSource](../../streamfontsource/) la clave de caché se define en las propiedades [CacheKey](../../memoryfontsource/get_cachekey/) y [CacheKey](../../streamfontsource/get_cachekey/) respectivamente. Para [FileFontSource](../../filefontsource/) la clave de caché es la propiedad [CacheKey](../../filefontsource/get_cachekey/) o una ruta de archivo si la [CacheKey](../../filefontsource/get_cachekey/) es **null**.

Se recomienda encarecidamente proporcionar los mismos orígenes de fuentes al cargar la caché que en el momento en que se guardó. Cualquier cambio en los orígenes de fuentes (p. ej., agregar nuevas fuentes, mover archivos de fuentes o cambiar la clave de caché) puede provocar una resolución inexacta de fuentes por parte de Aspose.Words.

## Ver también

* Class [FontSourceBase](../../fontsourcebase/)
* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
