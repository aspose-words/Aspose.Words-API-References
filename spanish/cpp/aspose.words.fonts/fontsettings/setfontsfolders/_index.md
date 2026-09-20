---
title: "Aspose::Words::Fonts::FontSettings::SetFontsFolders method"
linktitle: "SetFontsFolders"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fonts::FontSettings::SetFontsFolders method. Establece las carpetas donde Aspose.Words busca fuentes TrueType al renderizar documentos o incrustar fuentes en C++."
type: docs
weight: 12000
url: /es/cpp/aspose.words.fonts/fontsettings/setfontsfolders/
---
## FontSettings::SetFontsFolders method


Establece las carpetas donde Aspose.Words busca fuentes TrueType al renderizar documentos o incrustar fuentes.

```cpp
void Aspose::Words::Fonts::FontSettings::SetFontsFolders(const System::ArrayPtr<System::String> &fontsFolders, bool recursive)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fontsFolders | const System::ArrayPtr\<System::String\>\& | Una matriz de carpetas que contienen fuentes TrueType. |
| recursivo | bool | Verdadero para escanear las carpetas especificadas en busca de fuentes de forma recursiva. |
## Observaciones


Por defecto, Aspose.Words busca fuentes instaladas en el sistema.

Establecer esta propiedad restablece la caché de todas las fuentes cargadas previamente.

## Ejemplos



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

## Ver también

* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
