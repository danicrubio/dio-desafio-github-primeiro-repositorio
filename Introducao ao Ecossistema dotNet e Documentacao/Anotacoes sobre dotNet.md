# Anotações sobre .NET

#### Sobre .NET

.NET é um ecossistema, uma stack. É da Microsoft e é código aberto (open source).

.NET é uma plataforma cruzada, ou seja, permite desenvolver aplicações para diversos tipos de sistemas operacionais rodando sob diversas arquiteturas diferentes (x64, x32, ARM32, ARM64).

Para isso, a plataforma, o ecossistema .NET possui diversos tipos de implementações (.NET Framework, .NET Core, Xamarin).

**.NET Core** veio para tentar universalizar a criação dessas aplicações para Linux, Windows, Mac.

**.NET Framework** é um pouco mais acoplado ao sistema do Windows.

.NET Framework não vai evoluir mais, .NET Core é o futuro. Tem que ver o .NET Standard para fazer aplicações que possam interagir uma com a outra.



## Suporte ao desenvolvedor

#### Ambientes de desenvolvimento

Microsoft fornece o **Visual Studio**, que é um excelente ambiente de desenvolvimento com bastante ferramentas integradas. Porém é pesado e robusto (exige um pouco de memória do computador para isso) e só funciona para Mac e Windows. Por causa disso, criaram o Visual Studio Code que funciona em qualquer sistema operacional e é mais leve e pode adicionar plugins nele.



#### Linguagens de programação

A Microsoft produz **3 linguagens de programação:** C#, F# e Visual Basic.



#### Bibliotecas

Para rodar, para conseguirmos desenvolver alguma coisa, são necessárias bibliotecas.

- **SDK** (software development kit): biblioteca necessária para que se desenvolva aplicações na plataforma .NET.
- **Runtime**: é uma biblioteca necessária para que se execute essas aplicações.



#### NUGET

É um gerenciador de pacotes, consegue também baixar pacotes via prompt de comando e também tem interface gráfica.



#### Acesso a dados 

Tecnologias embutidas que ajudam o dev a programar consultas.

- **ORM** - Entity Framework Core: mapeador objeto relacional; dev pode pegar objeto ou entidade do código que está voltado ao paradigma orientado a objetos e o Entity Framework Core transforma isso em tabela; não precisa se preocupar em programar em SQL na mão por causa dele
- **LINQ** - consulta integrada à linguagem: padrão, sintaxe unificada para consultar os dados



#### Ambientes CI/CD

Integração contínua a partir desses ambientes que existem plug-ins dentro da plataforma .NET para facilitar.

- **GitHub Actions**

- **Azure Devops**

- **Cake/Fake**

  

#### Gerenciamento Automático de memória

Uso, alocação e desalocação de recursos; é chamado “coletor de lixo”, aloca um recurso para um objeto e não precisa se preocupar em desalocá-lo.



## ASP.NET e ASP.NET Core

ASP.NET Core foi lançado junto com o .NET Core e é uma evolução do ASP.NET. É um framework para desenvolvimento de Aplicações Web.

Bibliotecas para web patterns: mais conhecida é MVC (model-view-controller), que é bem utilizada pela separação de responsabilidades, reusabilidade de código.



## História do .NET

ASP.NET Web Forms que foi lançado em 2002 não era complexo, era focado em eventos e consistia em arrastar e soltar bloquinhos na tela. Porém os desenvolvedores não gostaram disso. Esse problema foi resolvido com o lançamento do ASP.NET MVC em 2007.

Lançamento do Xamarin demonstra olho no mercado mobile. A Microsoft ainda não havia adquirido o Xamarin, porém a empresa já havia sido fundada em 2011. Adquire a Xamarin em 2016.

Lançamento do ASP.NET MVC 5 em 2013, que depois daria lugar ao ASP.NET Core.

Em 2014, com o surgimento das aplicações nuvem, veio a Microsoft Azure. ASP.NET vNext foi o precursor do ASP.NET Core.



## Desenvolvimento Multiplataforma com .NET

Pode existir mais de um tipo de licença envolvida dentro. As licenças do .NET geralmente são MIT e Apache 2.

.NET Framework é muito acoplado ao Windows, o que fez com que criassem .NET Core pra ser multiplataforma. Aí veio o Xamarin para o mercado mobile.

Criaram uma especificação de APIs que as 3 implementações/frameworks entendem. Assim eles conseguem ter essa compatibilidade entre si. Mesmo tendo o .NET Standard, que é comum a todas essas plataformas, cada uma ainda possui o próprio tipo de biblioteca.



## .NET Standard

A Microsoft recomenda .NET Standard 2.0 (penúltima versão) já que está existindo essa transição de aplicações de .NET Framework pro .NET Core e pro .NET.

O .NET Core é o sucessor do .NET Framework. A necessidade de ter multiplataforma faz com que o .NET Framework seja descontinuado. Mas para os sistemas legados para ter compatibilidade, se recomenda usar o 2.0. A comunicação é bem ampla.

