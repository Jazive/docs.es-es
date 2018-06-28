---
title: Comando dotnet tool install - CLI de .NET Core
description: El comando dotnet tool install instala la herramienta global especificada de .NET Core en el equipo.
author: mairaw
ms.author: mairaw
ms.date: 05/29/2018
ms.openlocfilehash: f3068848910d6672a10ecfb639bac8e18a72818d
ms.sourcegitcommit: bbf70abe6b46073148f78cbf0619de6092b5800c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2018
ms.locfileid: "34697292"
---
# <a name="dotnet-tool-install"></a><span data-ttu-id="931f5-103">dotnet tool install</span><span class="sxs-lookup"><span data-stu-id="931f5-103">dotnet tool install</span></span>

[!INCLUDE [topic-appliesto-net-core-21plus.md](../../../includes/topic-appliesto-net-core-21plus.md)]

## <a name="name"></a><span data-ttu-id="931f5-104">nombre</span><span class="sxs-lookup"><span data-stu-id="931f5-104">Name</span></span>

<span data-ttu-id="931f5-105">`dotnet tool install`: instala la [herramienta global de .NET Core](global-tools.md) especificada en el equipo.</span><span class="sxs-lookup"><span data-stu-id="931f5-105">`dotnet tool install` - Installs the specified [.NET Core Global Tool](global-tools.md) on your machine.</span></span>

## <a name="synopsis"></a><span data-ttu-id="931f5-106">Sinopsis</span><span class="sxs-lookup"><span data-stu-id="931f5-106">Synopsis</span></span>

```
dotnet tool install <PACKAGE_NAME> <-g|--global> [--add-source] [--configfile] [--framework] [-v|--verbosity] [--version]
dotnet tool install <PACKAGE_NAME> <--tool-path> [--add-source] [--configfile] [--framework] [-v|--verbosity] [--version]
dotnet tool install <-h|--help>
```

## <a name="description"></a><span data-ttu-id="931f5-107">Description</span><span class="sxs-lookup"><span data-stu-id="931f5-107">Description</span></span>

<span data-ttu-id="931f5-108">El comando `dotnet tool install` permite instalar en el equipo herramientas globales de .NET Core.</span><span class="sxs-lookup"><span data-stu-id="931f5-108">The `dotnet tool install` command provides a way for you to install .NET Core Global Tools on your machine.</span></span> <span data-ttu-id="931f5-109">Para utilizar el comando, especifique que quiere una instalación en todos los usuarios con la opción `--global`, o bien especifique una ruta para instalarla usando para ello la opción `--tool-path`.</span><span class="sxs-lookup"><span data-stu-id="931f5-109">To use the command, you either have to specify that you want a user-wide installation using the `--global` option or you specify a path to install it using the `--tool-path` option.</span></span>

<span data-ttu-id="931f5-110">Las herramientas globales se instalan en los siguientes directorios de forma predeterminada cuando se especifica la opción `-g` (o `--global`):</span><span class="sxs-lookup"><span data-stu-id="931f5-110">Global Tools are installed in the following directories by default when you specify the `-g` (or `--global`) option:</span></span>

| <span data-ttu-id="931f5-111">SO</span><span class="sxs-lookup"><span data-stu-id="931f5-111">OS</span></span>          | <span data-ttu-id="931f5-112">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="931f5-112">Path</span></span>                          |
|-------------|-------------------------------|
| <span data-ttu-id="931f5-113">Linux/macOS</span><span class="sxs-lookup"><span data-stu-id="931f5-113">Linux/macOS</span></span> | `$HOME/.dotnet/tools`         |
| <span data-ttu-id="931f5-114">Windows</span><span class="sxs-lookup"><span data-stu-id="931f5-114">Windows</span></span>     | `%USERPROFILE%\.dotnet\tools` |

## <a name="arguments"></a><span data-ttu-id="931f5-115">Argumentos</span><span class="sxs-lookup"><span data-stu-id="931f5-115">Arguments</span></span>

`PACKAGE_NAME`

<span data-ttu-id="931f5-116">Nombre o identificador del paquete de NuGet que contiene la herramienta global de .NET Core que se quiere instalar.</span><span class="sxs-lookup"><span data-stu-id="931f5-116">Name/ID of the NuGet package that contains the .NET Core Global Tool to install.</span></span>

## <a name="options"></a><span data-ttu-id="931f5-117">Opciones</span><span class="sxs-lookup"><span data-stu-id="931f5-117">Options</span></span>

`--add-source <SOURCE>`

<span data-ttu-id="931f5-118">Agrega un origen de paquete NuGet adicional que se usará durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="931f5-118">Adds an additional NuGet package source to use during installation.</span></span>

`--configfile <FILE>`

<span data-ttu-id="931f5-119">El archivo de configuración de NuGet (*nuget.config*) que se usará.</span><span class="sxs-lookup"><span data-stu-id="931f5-119">The NuGet configuration (*nuget.config*) file to use.</span></span>

`--framework <FRAMEWORK>`

<span data-ttu-id="931f5-120">Especifica el [marco de destino](../../standard/frameworks.md) para instalar la herramienta.</span><span class="sxs-lookup"><span data-stu-id="931f5-120">Specifies the [target framework](../../standard/frameworks.md) to install the tool for.</span></span> <span data-ttu-id="931f5-121">De forma predeterminada, el SDK de .NET Core intenta elegir la plataforma de destino más apropiada.</span><span class="sxs-lookup"><span data-stu-id="931f5-121">By default, the .NET Core SDK tries to choose the most appropriate target framework.</span></span>

`-g|--global`

<span data-ttu-id="931f5-122">Especifica que la instalación se realiza en todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="931f5-122">Specifies that the installation is user wide.</span></span> <span data-ttu-id="931f5-123">No se puede combinar con la opción `--tool-path`.</span><span class="sxs-lookup"><span data-stu-id="931f5-123">Can't be combined with the `--tool-path` option.</span></span> <span data-ttu-id="931f5-124">Si no especifica esta opción, debe especificar la opción `--tool-path`.</span><span class="sxs-lookup"><span data-stu-id="931f5-124">If you don't specify this option, you must specify the `--tool-path` option.</span></span>

`-h|--help`

<span data-ttu-id="931f5-125">Imprime una corta ayuda para el comando.</span><span class="sxs-lookup"><span data-stu-id="931f5-125">Prints out a short help for the command.</span></span>

`--tool-path <PATH>`

<span data-ttu-id="931f5-126">Especifica la ubicación de donde se tiene que instalar la herramienta global.</span><span class="sxs-lookup"><span data-stu-id="931f5-126">Specifies the location where to install the Global Tool.</span></span> <span data-ttu-id="931f5-127">PATH puede ser una ruta absoluta o relativa.</span><span class="sxs-lookup"><span data-stu-id="931f5-127">PATH can be absolute or relative.</span></span> <span data-ttu-id="931f5-128">Si la ruta no existe, el comando intenta crearla.</span><span class="sxs-lookup"><span data-stu-id="931f5-128">If PATH doesn't exist, the command tries to create it.</span></span> <span data-ttu-id="931f5-129">No se puede combinar con la opción `--global`.</span><span class="sxs-lookup"><span data-stu-id="931f5-129">Can't be combined with the `--global` option.</span></span> <span data-ttu-id="931f5-130">Si no especifica esta opción, debe especificar la opción `--global`.</span><span class="sxs-lookup"><span data-stu-id="931f5-130">If you don't specify this option, you must specify the `--global` option.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="931f5-131">Establece el nivel de detalle del comando.</span><span class="sxs-lookup"><span data-stu-id="931f5-131">Sets the verbosity level of the command.</span></span> <span data-ttu-id="931f5-132">Los valores permitidos son `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` y `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="931f5-132">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span>

`--version <VERSION_NUMBER>`

<span data-ttu-id="931f5-133">La versión de la herramienta que se va instalar.</span><span class="sxs-lookup"><span data-stu-id="931f5-133">The version of the tool to install.</span></span> <span data-ttu-id="931f5-134">De forma predeterminada, se instala la versión estable más reciente del paquete.</span><span class="sxs-lookup"><span data-stu-id="931f5-134">By default, the latest stable package version is installed.</span></span> <span data-ttu-id="931f5-135">Utilice esta opción para instalar la versión preliminar o versiones anteriores de la herramienta.</span><span class="sxs-lookup"><span data-stu-id="931f5-135">Use this option to install preview or older versions of the tool.</span></span>

## <a name="examples"></a><span data-ttu-id="931f5-136">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="931f5-136">Examples</span></span>

<span data-ttu-id="931f5-137">Instala la herramienta global [dotnetsay](https://www.nuget.org/packages/dotnetsay/) en la ubicación predeterminada:</span><span class="sxs-lookup"><span data-stu-id="931f5-137">Installs the [dotnetsay](https://www.nuget.org/packages/dotnetsay/) Global Tool in the default location:</span></span>

`dotnet tool install -g dotnetsay`

<span data-ttu-id="931f5-138">Instala la herramienta global [dotnetsay](https://www.nuget.org/packages/dotnetsay/) en una carpeta específica de Windows:</span><span class="sxs-lookup"><span data-stu-id="931f5-138">Installs the [dotnetsay](https://www.nuget.org/packages/dotnetsay/) Global Tool on a specific Windows folder:</span></span>

`dotnet tool install dotnetsay --tool-path c:\global-tools`

<span data-ttu-id="931f5-139">Instala la herramienta global [dotnetsay](https://www.nuget.org/packages/dotnetsay/) en una carpeta específica de Linux/macOS:</span><span class="sxs-lookup"><span data-stu-id="931f5-139">Installs the [dotnetsay](https://www.nuget.org/packages/dotnetsay/) Global Tool on a specific Linux/macOS folder:</span></span>

`dotnet tool install dotnetsay --tool-path ~/bin`

<span data-ttu-id="931f5-140">Instala la versión 2.0.0 de la herramienta global [dotnetsay](https://www.nuget.org/packages/dotnetsay/):</span><span class="sxs-lookup"><span data-stu-id="931f5-140">Installs version 2.0.0 of the [dotnetsay](https://www.nuget.org/packages/dotnetsay/) Global Tool:</span></span>

`dotnet tool install -g dotnetsay --version 2.0.0`

## <a name="see-also"></a><span data-ttu-id="931f5-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="931f5-141">See also</span></span>

[<span data-ttu-id="931f5-142">Herramientas globales de .NET Core</span><span class="sxs-lookup"><span data-stu-id="931f5-142">.NET Core Global Tools</span></span>](global-tools.md)