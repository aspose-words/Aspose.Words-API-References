---
title: "Aspose::Words::Fonts::FontSettings class"
linktitle: "FontSettings"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Fonts::FontSettings. Especifica la configuración de fuentes para un documento. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words.fonts/fontsettings/
---
## FontSettings class


Especifica la configuración de fuentes para un documento. Para obtener más información, visite el artículo de documentación [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FontSettings : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [FontSettings](./fontsettings/)() |  |
| static [get_DefaultInstance](./get_defaultinstance/)() | Configuración de fuentes predeterminada estática. |
| [get_FallbackSettings](./get_fallbacksettings/)() const | [Configuración](../../aspose.words.settings/) relacionada con el mecanismo de reserva de fuentes. |
| [get_SubstitutionSettings](./get_substitutionsettings/)() const | [Configuración](../../aspose.words.settings/) relacionada con el mecanismo de sustitución de fuentes. |
| [GetFontsSources](./getfontssources/)() | Obtiene una copia de la matriz que contiene la lista de fuentes donde Aspose.Words busca fuentes TrueType. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ResetFontSources](./resetfontsources/)() | Restablece las fuentes a la configuración predeterminada del sistema. |
| [SaveSearchCache](./savesearchcache/)(const System::SharedPtr\<System::IO::Stream\>\&) | Guarda la caché de búsqueda de fuentes en el flujo. |
| [SetFontsFolder](./setfontsfolder/)(const System::String\&, bool) | Establece la carpeta donde Aspose.Words busca fuentes TrueType al renderizar documentos o incrustar fuentes. Esto es un acceso directo a [SetFontsFolders()](../) para establecer solo un directorio de fuentes. |
| [SetFontsFolders](./setfontsfolders/)(const System::ArrayPtr\<System::String\>\&, bool) | Establece las carpetas donde Aspose.Words busca fuentes TrueType al renderizar documentos o incrustar fuentes. |
| [SetFontsSources](./setfontssources/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\&) | Establece las fuentes donde Aspose.Words busca fuentes TrueType al renderizar documentos o incrustar fuentes. |
| [SetFontsSources](./setfontssources/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\&, const System::SharedPtr\<System::IO::Stream\>\&) | Establece las fuentes donde Aspose.Words busca fuentes TrueType y, adicionalmente, carga la caché de búsqueda de fuentes guardada previamente. |
| static [Type](./type/)() |  |
## Observaciones


Aspose.Words utiliza la configuración de fuentes para resolver las fuentes en el documento. [Fuentes](../) se resuelven principalmente al crear el diseño del documento o al renderizar a formatos de página fija. Pero al cargar algunos formatos, Aspose.Words también puede necesitar resolver las fuentes. Por ejemplo, al cargar documentos HTML, Aspose.Words puede resolver las fuentes para realizar la reserva de fuentes. Por lo tanto, se recomienda que establezca la configuración de fuentes en [LoadOptions](../../aspose.words.loading/loadoptions/) al cargar el documento. O al menos antes de crear el diseño o renderizar el documento al formato de página fija.

Por defecto, todos los documentos usan una única instancia estática de configuración de fuentes. Se puede acceder a ella mediante la propiedad [DefaultInstance](./get_defaultinstance/).

Cambiar la configuración de fuentes es seguro en cualquier momento y desde cualquier hilo. Pero se recomienda no cambiar la configuración de fuentes mientras se procesan algunos documentos que utilizan esta configuración. Esto puede provocar que la misma fuente se resuelva de manera diferente en distintas partes del documento.

## Ejemplos



Mostrar cómo establecer un directorio de origen de fuentes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arvo");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Amethysta");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

// Nuestras fuentes de origen no contienen la fuente que hemos utilizado para el texto en este documento.
// Si usamos esta configuración de fuentes al renderizar este documento,
// Aspose.Words aplicará una fuente de respaldo al texto que tenga una fuente que Aspose.Words no pueda localizar.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> originalFontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_EQ(1, originalFontSources->get_Length());
ASSERT_TRUE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));

// Las fuentes de origen predeterminadas no incluyen las dos fuentes que estamos usando en este documento.
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arvo";
}))));
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));

// Utilice el método "SetFontsFolder" para establecer un directorio que actuará como una nueva fuente de fuentes.
// Pase "false" como argumento "recursive" para incluir fuentes de todos los archivos de fuentes que están en el directorio
// que estamos pasando como primer argumento, pero sin incluir fuentes en ninguna de las subcarpetas de ese directorio.
// Pase "true" como argumento "recursive" para incluir todos los archivos de fuentes en el directorio que estamos pasando
// como primer argumento, así como todas las fuentes en sus subdirectorios.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsFolder(get_FontsDir(), recursive);

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> newFontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_EQ(1, newFontSources->get_Length());
ASSERT_FALSE(newFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));
ASSERT_TRUE(newFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arvo";
}))));

// La fuente "Amethysta" está en una subcarpeta del directorio de fuentes.
if (recursive)
{
    ASSERT_EQ(30, newFontSources[0]->GetAvailableFonts()->get_Count());
    ASSERT_TRUE(newFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
    {
        return f->get_FullFontName() == u"Amethysta";
    }))));
}
else
{
    ASSERT_EQ(18, newFontSources[0]->GetAvailableFonts()->get_Count());
    ASSERT_FALSE(newFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
    {
        return f->get_FullFontName() == u"Amethysta";
    }))));
}

doc->Save(get_ArtifactsDir() + u"FontSettings.SetFontsFolder.pdf");

// Restaurar las fuentes de origen originales.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsSources(originalFontSources);
```


Mostrar cómo establecer múltiples directorios de origen de fuentes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Amethysta");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");
builder->get_Font()->set_Name(u"Junction Light");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

// Nuestras fuentes de origen no contienen la fuente que hemos utilizado para el texto en este documento.
// Si usamos esta configuración de fuentes al renderizar este documento,
// Aspose.Words aplicará una fuente de respaldo al texto que tenga una fuente que Aspose.Words no pueda localizar.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> originalFontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_EQ(1, originalFontSources->get_Length());
ASSERT_TRUE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));

// Las fuentes de origen predeterminadas no incluyen las dos fuentes que estamos usando en este documento.
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Junction Light";
}))));

// Utilice el método "SetFontsFolders" para crear una fuente de fuentes a partir de cada directorio de fuentes que pasamos como primer argumento.
// Pase "false" como argumento "recursive" para incluir fuentes de todos los archivos de fuentes que están en los directorios
// que estamos pasando como primer argumento, pero sin incluir fuentes de ninguna de las subcarpetas de los directorios.
// Pase "true" como argumento "recursive" para incluir todos los archivos de fuentes en los directorios que estamos pasando
// como primer argumento, así como todas las fuentes en sus subdirectorios.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsFolders(System::MakeArray<System::String>({get_FontsDir() + u"/Amethysta", get_FontsDir() + u"/Junction"}), recursive);

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> newFontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_EQ(2, newFontSources->get_Length());
ASSERT_FALSE(newFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));
ASSERT_EQ(1, newFontSources[0]->GetAvailableFonts()->get_Count());
ASSERT_TRUE(newFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));

// La carpeta "Junction" en sí no contiene archivos de fuentes, pero tiene subcarpetas que sí los contienen.
if (recursive)
{
    ASSERT_EQ(11, newFontSources[1]->GetAvailableFonts()->get_Count());
    ASSERT_TRUE(newFontSources[1]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
    {
        return f->get_FullFontName() == u"Junction Light";
    }))));
}
else
{
    ASSERT_EQ(0, newFontSources[1]->GetAvailableFonts()->get_Count());
}

doc->Save(get_ArtifactsDir() + u"FontSettings.SetFontsFolders.pdf");

// Restaurar las fuentes de origen originales.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsSources(originalFontSources);
```


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

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
