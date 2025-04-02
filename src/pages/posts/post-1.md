---
layout: '../../layouts/BlogPostLayout.astro'
title: Build a production-ready multiplayer game with Netcode for GameObjects
pubDate: "2022-07-01"
minRead: "7 MIN"
description: 'Este artículo explora cómo construir un juego multijugador listo para producción utilizando Unity y Netcode for GameObjects.'
author: 'Gabriel Calderón'
authorDescription: "Game Developer"
authorSocial: 'https://github.com/ga-b0/'
imageAuthor: 
    url: 'https://live.staticflickr.com/65535/53834601272_b6d926f0e9_n.jpg'
    alt: 'Gabriel Calderón'
image:
    url: 'https://images.unsplash.com/photo-1550745165-9bc0b252726f?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D'
    alt: 'El logotipo completo de Astro.'
tags: ["Unity", "Multijugador", "Netcode for GameObjects", "Desarrollo de Juegos"]
---

En esta serie de cuatro partes, exploramos cómo puedes construir un juego multijugador listo para producción utilizando Unity y **Netcode for GameObjects (NGO)**. A través de un análisis del juego de muestra *Boss Room*, aprenderás las mejores prácticas y consejos clave para desarrollar un juego multijugador escalable y optimizado.

## 1. **Entender la implementación básica del juego y la autoridad del servidor**

En el primer episodio, cubrimos las mejores prácticas y consejos cuando introduces tecnologías como internet para el desarrollo de un juego multijugador. Hablamos de:

- **¿Qué es Netcode for GameObjects (NGO)** y **Unity Gaming Services (UGS)**?
- **NetworkVariables** vs **RPCs**: Cuándo usar cada uno y por qué.
- Autoridad en el servidor: Por qué elegimos la autoridad del servidor para la mayoría de nuestras mecánicas de juego.
- Movimientos y modelos alternativos como **Client Authority** para manejar el lag y trucos de optimización para movimientos basados en **pathfinding**.
- Implementación básica del juego: Cómo usamos el **State (netvar, network list)** y los **RPCs**.

## 2. **Construir habilidades de personajes, aparición y objetos de escena**

En el segundo episodio, profundizamos en la implementación de habilidades de personajes y cómo puedes implementarlas en tu propio juego. Algunos temas que tocamos incluyen:

- El flujo general para implementar habilidades impulsadas por el servidor.
- La fiabilidad de los **RPCs** y cómo tratar con **RPCs no fiables**.
- Ataques cuerpo a cuerpo y la anticipación de problemas con animaciones.
- Funcionalidad del escudo de tanque y su interacción con el entorno.
- Poderes de arco y disparos de área de efecto (AOE).
- Sistema de habilidades para magos, como el uso de **firebolt** y optimización del uso del ancho de banda.

También cubrimos la dinámica de la aparición de objetos:

- Aparición de objetos **dinámicamente**.
- Aparición de objetos **estáticos** en la escena.
- Objetos **destructibles** en la escena.
- Lecciones aprendidas sobre la aparición de enemigos, como los **zombie imps**, al unirse tarde al juego.

## 3. **Hacer tu juego multijugador resiliente a los jugadores**

En el tercer episodio, tratamos más detalles sobre la implementación del juego antes de enfocarnos en cómo hacer que tu juego sea más resistente a los problemas comunes de los jugadores. Aquí abordamos:

- Interacciones físicas, objetos y jerarquías, así como la gestión de escenas.
- Uso de **Relay y Lobby** para poner tu juego en línea y por qué **NGO** no es adecuado para jugadores que se unen a mitad del juego.
- Sincronización de la pantalla de selección de personajes entre jugadores usando **NGO** y **serialización personalizada**.
- Soporte de reconexión, manejo de **caídas de conexión**, flujos de reconexión y soporte para unirse tarde al juego.
- Manejo de condiciones de carrera y pruebas para asegurar la fiabilidad de los procesos.

## 4. **Optimizar el ancho de banda y los procesos de desarrollo de juegos**

En el cuarto y último episodio, exploramos las mejores prácticas en el desarrollo de juegos multijugador, incluyendo:

- **Optimización del ancho de banda**: Herramientas para perfilar el uso del ancho de banda y optimizar **NetworkTransforms**.
- Herramientas de depuración como **simuladores de condiciones de red**, monitoreo de estadísticas y flujos de depuración personalizados.
- Arquitectura del proyecto: sistemas de acción, arquitectura de jugadores y más.
- El futuro de **Boss Room** y cómo planeamos evolucionar este sistema.

¡Con estos cuatro episodios, estarás listo para crear tu propio juego multijugador usando **Netcode for GameObjects** en Unity!

![Boss Room Gameplay](https://images.unsplash.com/photo-1580617971627-cffa74e39d1d?q=80&w=2153&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D)
