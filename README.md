# Tutorial de Julia

## Tabla de contenidos

1. Instalaciones:
    - [Julia](https://julialang.org/downloads/) 
    - [Git](https://git-scm.com/downloads)
    - Editor de texto
        - [Opcional] Extensiones editor de texto útiles (VSCode)
    - Paquetes de Julia comunmente usados
2. Aprendiendo lo básico:
    - Arrays, Strings, etc.
    - For loops
    - Funciones
    - Cómo escribir código eficiente en Julia.
    - Utilizar Benchmarks y comparar con otros lenguajes dinámicos populares (Python, R, Matlab, etc)
3. Modelando problemas de optimización en Julia.
    - LPs
    - [Optimización Cónica](https://danpereda.github.io/post/conicopt/).
4. [Machine Learning científico](https://danpereda.github.io/post/scientificmachinelearning/)
    - Resolver EDOS en Julia
    - Resolver SDE en Julia
    - Inferencia paramétrica en EDOS
    - Neural ODEs
    - Resolución de EDOS con redes neuronales (Physics - informed neural networks)

## Instalaciones

### Instalando Julia

[Click aquí para descargar Julia](https://julialang.org/downloads/) *Current Stable release : v1.5.0* al momento de realizar este workshop, ha sido confirmado en JuliaCon2020 que Julia v1.6.0 será lanzado a fines de 2020 y será la nueva versión estable y de largo plazo. Comparado con la versión v1.4 se disminuye la latencia en más de un 50% lo que influye en los tiempos de compilación.

Otra opción es descargar [Julia PRO](https://juliacomputing.com/products/juliapro.html), el cual contiene Julia + Juno IDE + Atom + algunos paquetes.

### Git

Se recomienda instalar también [Git](https://git-scm.com/downloads) junto con [Github Desktop](https://desktop.github.com/) (recomendado para nuevos usuarios) y opcionalmente para aprender un poco más de Github y trabajar en proyectos con más personas [GitKraken](https://www.gitkraken.com/).

*Nota: Para seguir el problema de la cantidad mínima de pasaportes es necesario instalar Git*

### Editors and IDEs

Si no estás acostumbrado a usar un editor en particular, recomiendo instalar VS Code. [Instrucciones](https://www.julia-vscode.org/). 

Editores de texto más populares (Juno, VS Code, Jupyter, JetBrains, Vim, Emacs, SublimeText, NotePad++) son compatibles con Julia  [ver sección Editors and IDEs](https://julialang.org/) para tener una guía de cómo instalar cada uno.

Para utilizar Jupyter Notebooks se requiere instalar el paquete `IJulia.jl`. Para esto, abrir Julia y correr el siguiente código en Julia REPL (Julia's interactive command prompt).

```julia
import Pkg
Pkg.add("IJulia") # Solo la primera vez
using IJulia # Estas últimas 2 líneas son las que se utilizarán normalmente para trabajar con Jupyter Notebooks en Julia
notebook()
```

En caso de no tener instalado Jupyter, se debe correr primero el siguiente código en Julia REPL:

```julia
import Pkg
ENV["JUPYTER"]=""
Pkg.add("Conda")
Pkg.add("IJulia")
import Conda
Conda.add("jupyter")
```

#### Extensiones útiles en VS Code

Las siguientes extensiones mejoran la calidad de vida al programar en VS Code, son en su mayoría mejoras visuales, agregando colores a cada par de paréntesis y destacando que es lo que está escrito dentro de ellos, muestra con distintos colores las identaciones, se pueden cambiar nombres de todas las ocurrencias de una palabra de manera automática, etc.

    - Material Theme Icons 
    - Format in context menus
    - Bracker Pair Colorizer 2
    - Indent-rainbow
    - Auto Rename Tag

### Paquetes de Julia comúnmente utilizados

Para uso general se tienen los paquetes `LinearAlgebra.jl` y `Plots.jl`.

Para Optimización se utiliza mucho el paquete `JuMP.jl` que es para escribir modelos de manera eficiente. Muchos de los demás paquetes de optimización están conectados a este.

Para Ecuaciones Diferenciales el paquete principal es `DifferentialEquations`.
Muchos de los demás paquetes de ecuaciones diferenciales están conectados a este.

Una lista de los paquetes más populares y documentación se puede encontrar en [JuliaHub](https://juliahub.com/ui/Home), página muy recomendada.

Se recomienda correr el siguiente código para obtener todos los paquetes necesarios para el WorkShop

```julia
using Pkg
Pkg.add("LinearAlgebra")
Pkg.add("BenchmarkTools")
Pkg.add("Plots")
Pkg.add("JuMP")
Pkg.add("DifferentialEquations")
Pkg.add("Sundials") # Solver de EDO's con mucho stiff a baja tolerancia
Pkg.add("Optim") # Solvers de Optimización
Pkg.add("Flux")
Pkg.add("DiffEqFlux")
Pkg.add("Turing")
Pkg.add("Distributions")
Pkg.add("DataFrames")
Pkg.add("DiffEqSensitivity")
Pkg.add("MCMCChains")
Pkg.add("StatsPlots")
Pkg.add("Random")
Pkg.add("IJulia")
Pkg.add("OrdinaryDiffEq")
Pkg.add("ModelingToolkit")
Pkg.add("DataDrivenDiffEq")
Pkg.add("JLD2")
Pkg.add("NeuralPDE")
Pkg.add("ECOS")
Pkg.add("CSV")
Pkg.add("HTTP")
Pkg.add("Tables")
Pkg.add("DataFrames")
Pkg.add("Dates")
Pkg.add("XLSX")
```

## Aprendiendo lo básico

Descargar el siguiente [Jupyter Notebook](https://github.com/danpereda/Julia-Wokshop-435/blob/master/Jupyter%20Notebooks/AprendiendoJulia.ipynb).

## Optimización

Descargar el siguiente Jupyter Notebook

## Machine Learning Científico

Descargar el siguiente Jupyter Notebook