# Proyecto-SPA-BOP
Projecte de gestió i automatització d’un SPA, desenvolupat per gestionar clients, cites i serveis.
# SPA - Gestor de Citas y Servicios

Aplicación web para la **gestión y automatización de la agenda de un SPA**. El sistema permite administrar clientes, citas, servicios, pagos y un sistema de fidelización mediante puntos.

## Funcionalidades

* Gestión y registro de clientes.
* Creación, modificación y cancelación de citas.
* Selección de uno o varios servicios por cita.
* Cálculo de la duración y hora prevista de salida.
* Validación de citas según el horario del establecimiento.
* Registro de servicios realizados.
* Generación y gestión de tiquets de cobro.
* Sistema de puntos de fidelización.
* Servicio gratuito al alcanzar **100 puntos**.

## Servicios

El SPA ofrece los siguientes servicios:

| Servicio | Descripción           |
| -------- | --------------------- |
| Solàrium | Servicio de solárium  |
| Massatge | Servicio de masaje    |
| Estètica | Servicios de estética |

Cada servicio dispone de:

* Nombre
* Descripción
* Precio
* Duración
* Puntos de recompensa

## Horario del SPA

| Día             | Horario       |
| --------------- | ------------- |
| Lunes - Viernes | 08:00 - 20:00 |
| Sábado          | 09:00 - 15:00 |
| Domingo         | Cerrado       |

Las citas únicamente pueden realizarse dentro del horario de apertura.

## Gestión de citas

Al solicitar una cita, el cliente debe indicar:

* Día y hora.
* Servicios que desea realizar.

El sistema comprueba que la cita pueda realizarse dentro del horario disponible y calcula la **hora prevista de salida**.

Las citas pueden cancelarse hasta **24 horas antes** de la fecha y hora reservadas.

> Para simplificar el proyecto, no se controla la disponibilidad individual de cada servicio.

## Sistema de fidelización

Los clientes acumulan puntos por cada servicio realizado.

Cuando un cliente alcanza **100 puntos**, puede obtener **un servicio gratuito**.

## Objetivo del proyecto

El objetivo es desarrollar una aplicación que facilite la gestión diaria del SPA, centralizando en un único sistema la información de clientes, citas, servicios, pagos y fidelización.

## Tecnologías

* **Frontend:** Angular
* **Backend:** Laravel
* **Base de datos:** MySQL
* **Contenedores:** Docker
* **Control de versiones:** Git / GitHub

## Estructura general

```text
SPA/
├── frontend/       # Aplicación Angular
├── backend/        # API php
├── database/       # Base de datos y migraciones
├── docker/         # Configuración Docker
└── README.md
```

## Instalación

### 1. Clonar el repositorio

```bash
git clone <URL_DEL_REPOSITORIO>
cd SPA
```

### 2. Iniciar los contenedores

```bash
docker compose up -d
```

### 3. Configurar el Backend

```bash
cd backend
composer install
cp .env.example .env
php artisan key:generate
php artisan migrate
```

### 4. Iniciar Angular

```bash
cd frontend
npm install
ng serve
```

La aplicación estará disponible en:

```text
http://localhost:4200
```

## Estado del proyecto

**En desarrollo**

Este proyecto forma parte de un proyecto académico de desarrollo **Full Stack** utilizando Angular, Laravel y Docker.

## Autores

Proyecto desarrollado como parte del **Proyecto Final de Estudios**.
