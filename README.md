#rutas 
!DOCTYPE html>
<html lang="es">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rutas de Transporte</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }

        header {
            background-color: #0066cc;
            color: white;
            text-align: center;
            padding: 1rem;
        }

        nav {
            background-color: #004080;
            padding: 0.5rem;
        }

        nav ul {
            list-style-type: none;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
        }

        nav li {
            margin: 0 1rem;
        }

        nav a {
            color: white;
            text-decoration: none;
            padding: 0.5rem;
        }

        nav a:hover {
            background-color: #0066cc;
            border-radius: 4px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 1rem;
        }

        .search-container {
            background-color: white;
            padding: 1rem;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
            margin-bottom: 1.5rem;
        }

        .search-box {
            display: flex;
            gap: 10px;
            margin-bottom: 10px;
        }

        .search-input {
            flex: 1;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 4px;
            font-size: 16px;
        }

        .search-button {
            background-color: #0066cc;
            color: white;
            border: none;
            border-radius: 4px;
            padding: 10px 20px;
            cursor: pointer;
            font-size: 16px;
        }

        .search-button:hover {
            background-color: #004080;

        }

        .filter-checkbox input {
            margin-right: 5px;
        }

        .route-card {
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
            margin-bottom: 1.5rem;
            overflow: hidden;
        }

        .route-header {
            background-color: #004080;
            color: white;
            padding: 1rem;
            font-size: 1.2rem;
        }

        .stops-list {
            background-color: #f9f9f9;
            padding: 1rem;
            border-radius: 4px;
            margin-top: 1rem;
        }

        .bus-features {
            margin-top: 1rem;
            background-color: #e6f2ff;
            padding: 1rem;
            border-radius: 4px;
        }

        .feature-list {
            list-style-type: none;
            padding-left: 0;
        }

        .feature-list li {
            margin-bottom: 0.5rem;
            padding-left: 1.5rem;
            position: relative;
        }

        .feature-list li::before {
            content: "✓";
            color: #0066cc;
            position: absolute;
            left: 0;
        }

        footer {
            background-color: #004080;
            color: white;
            text-align: center;
            padding: 1rem;
            margin-top: 2rem;
        }

        .no-results {
            text-align: center;
            padding: 2rem;
            background-color: white;
            border-radius: 8px;
            margin-bottom: 1.5rem;
        }

        .highlight {
            background-color: #ffff99;
            font-weight: bold;
        }

        @media (max-width: 768px) {
            .route-content {
                flex-direction: column;
            }

            nav ul {
                flex-direction: column;
                align-items: center;
            }

            nav li {
                margin: 0.5rem 0;
            }

            .search-box {
                flex-direction: column;
            }
        }
    </style>
</head>

<body>
    <header>
        <h1>RutasFácil</h1>
        <p>Información completa sobre rutas de transporte público</p>
    </header>

    <div class="container">
        <!-- Búsqueda -->
        <div class="search-container">
            <h2>Buscar Rutas</h2>
            <div class="search-box">
                <input type="text" id="search-input" class="search-input"
                    placeholder="Buscar por número de ruta, nombre o parada...">
                <button id="search-button" class="search-button">Buscar</button>
            </div>
        </div>

        <h2>Rutas Disponibles</h2>
        <div id="routes-container">
            <!-- Ruta 1 -->
            <div class="route-card" data-route="29 pch c"
                data-stops=" Central, Cubitos, Hospital General, Seguro Social, Avila Camacho">
                <div class="route-header">
                    Ruta 29 PCH C - A. Camacho a Central
                </div>
                <div class="route-content">
                    <div class="route-info">
                        <h3>Características del Transporte</h3>
                        <div class="bus-features">
                            <ul class="feature-list">
                                <li>Horario: 5:00 AM - 11:00 PM</li>
                                <li>Frecuencia: Cada 15 minutos</li>
                            </ul>
                        </div>

                        <h3>Paradas</h3>
                        <div class="stops-list">
                            <ol>
                                <li>Central de Autobuses</li>
                                <li>Cubitos</li>
                                <li>Hospital General </li>
                                <li>Seguro Social</li>
                                <li>Avila Camacho</li>

                        </div>
                    </div>

                    <div class="route-media">
                        <h3>Modelo de la combi </ 29 PCH C <h3>
                            <img src="https://1drv.ms/i/c/bd58d539dbf23a32/IQTOu3ZPUZd2RrLikg9r_1QUAT3Ty1usDTM8XdmFdIRciZ0?width=660"
                                width="660" height="auto" />

                            <h3>Mapa de la Ruta</h3>

                            <p><small>Haz clic en el mapa para ver la ruta en Google Maps</small></p>
                    </div>
                    <div class="u-container-style u-layout-cell u-right-cell u-size-30 u-layout-cell-2">
                        <div class="u-container-layout u-container-layout-2">
                            <div class="u-expanded u-grey-10 u-map">
                                <div class="embed-responsive">
                                    <iframe class="embed-responsive-item"
                                        src="https://www.google.com/maps/embed?pb=!1m56!1m12!1m3!1d59944.58989404574!2d-98.77033063578907!3d20.111637917182183!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!4m41!3e0!4m3!3m2!1d20.106468!2d-98.751719!4m3!3m2!1d20.105558!2d-98.745111!4m3!3m2!1d20.113688!2d-98.73389499999999!4m3!3m2!1d20.117606!2d-98.730319!4m3!3m2!1d20.114552!2d-98.72480499999999!4m3!3m2!1d20.111271!2d-98.722145!4m3!3m2!1d20.111539999999998!2d-98.715612!4m3!3m2!1d20.111638!2d-98.712609!4m3!3m2!1d20.111735!2d-98.710049!4m3!3m2!1d20.112147999999998!2d-98.70450199999999!5e0!3m2!1ses-419!2smx!4v1745211205553!5m2!1ses-419!2smx"
                                        data-map="JTdCJTIycG9zaXRpb25UeXBlJTIyJTNBJTIybWFwLWVtYmVkJTIyJTJDJTIyYWRkcmVzcyUyMiUzQSUyMk1hbmhhdHRhbiUyMiUyQyUyMnpvb20lMjIlM0FudWxsJTJDJTIydHlwZUlkJTIyJTNBJTIycm9hZCUyMiUyQyUyMmxhbmclMjIlM0FudWxsJTJDJTIyYXBpS2V5JTIyJTNBbnVsbCUyQyUyMm1hcmtlcnMlMjIlM0ElNUIlNUQlMkMlMjJlbWJlZCUyMiUzQSUyMmh0dHBzJTNBJTJGJTJGd3d3Lmdvb2dsZS5jb20lMkZtYXBzJTJGZW1iZWQlM0ZwYiUzRCExbTU2ITFtMTIhMW0zITFkNTk5NDQuNTg5ODk0MDQ1NzQhMmQtOTguNzcwMzMwNjM1Nzg5MDchM2QyMC4xMTE2Mzc5MTcxODIxODMhMm0zITFmMCEyZjAhM2YwITNtMiExaTEwMjQhMmk3NjghNGYxMy4xITRtNDEhM2UwITRtMyEzbTIhMWQyMC4xMDY0NjghMmQtOTguNzUxNzE5ITRtMyEzbTIhMWQyMC4xMDU1NTghMmQtOTguNzQ1MTExITRtMyEzbTIhMWQyMC4xMTM2ODghMmQtOTguNzMzODk0OTk5OTk5OTkhNG0zITNtMiExZDIwLjExNzYwNiEyZC05OC43MzAzMTkhNG0zITNtMiExZDIwLjExNDU1MiEyZC05OC43MjQ4MDQ5OTk5OTk5OSE0bTMhM20yITFkMjAuMTExMjcxITJkLTk4LjcyMjE0NSE0bTMhM20yITFkMjAuMTExNTM5OTk5OTk5OTk4ITJkLTk4LjcxNTYxMiE0bTMhM20yITFkMjAuMTExNjM4ITJkLTk4LjcxMjYwOSE0bTMhM20yITFkMjAuMTExNzM1ITJkLTk4LjcxMDA0OSE0bTMhM20yITFkMjAuMTEyMTQ3OTk5OTk5OTk4ITJkLTk4LjcwNDUwMTk5OTk5OTk5ITVlMCEzbTIhMXNlcy00MTkhMnNteCE0djE3NDUyMTEyMDU1NTMhNW0yITFzZXMtNDE5ITJzbXglMjIlN0Q="></iframe>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Ruta 2 -->
            <div class="route-card" data-route="18 PCH C"
                data-stops="Paseos de Chavarría, Tuzos, Tulipanes, El Venado, La Calera, La Providencia, San Carlos, Camelinas, Santa Catarina, Morelos, Piracantos, El Palmar, Centro de Pachuca">
                <div class="route-header">
                    18 PCH C
                </div>
                <div class="route-content">
                    <div class="route-info">
                        <h3>Características del Transporte</h3>
                        <div class="bus-features">
                            <ul class="feature-list">

                                <li>Horario: 6:00 AM - 10:00 PM</li>
                                <li>Frecuencia: Cada 10 minutos</li>
                            </ul>
                        </div>

                        <h3>Paradas</h3>
                        <div class="stops-list">
                            <ol>
                                <li>Paseos de Chavarría</li>
                                <li>Tuzos</li>
                                <li>Tulipanes</li>
                                <li>El Venado</li>
                                <li>La Calera</li>
                                <li>La Providencia</li>
                                <li>San Carlos</li>
                                <li>Camelinas</li>
                                <li>Santa Catarina</li>
                                <li>Morelos</li>
                                <li>Piracantos</li>
                                <li>El Palmar</li>
                                <li>Centro de Pachuca</li>
                                                         </ol>
                            <p><small>* Los horarios son aproximados y se repiten cada 10 minutos</small></p>
                        </div>
                    </div>

                    <div class="route-media">
                        <h3>Minibús de la Ruta 15</h3>
                        <img src="c:\Users\julianee\OneDrive\Pictures\pagina web\Imagen de WhatsApp 2025-04-27 a las 14.29.16_a71c9d1c.jpg"
                            alt="Minibús de la Ruta 15" class="route-image">

                        <h3>Mapa de la Ruta</h3>
                        <p><small>Haz clic en el mapa para ver la ruta en Google Maps</small></p>
                    </div>
                    <div class="u-clearfix u-custom-html u-custom-html-1">
                        <iframe
                            src="https://www.google.com/maps/d/u/1/embed?mid=1Hwq66aTIjNhInFj-aRLx3ou0V53X_sU&amp;ehbc=2E312F&amp;noprof=1"
                            width="560" height="640"></iframe>
                    </div>
                </div>
            </div>

            <!-- Ruta 3 -->
            <div class="route-card" data-route="28" data-features="wifi,ac"
                data-stops="Terminal Oeste,Parque Industrial,Centro Financiero,Hospital Universitario,Plaza Comercial,Campus Universitario">
                <div class="route-header">
                    Ruta 28 - Oeste a Este
                </div>
                <div class="route-content">
                    <div class="route-info">
                        <h3>Características del Transporte</h3>
                        <div class="bus-features">
                            <ul class="feature-list">
                                <li>WiFi gratuito</li>
                                <li>Aire acondicionado</li>
                                <li>Capacidad para 50 pasajeros</li>
                                <li>Puertos USB para carga de dispositivos</li>
                                <li>Horario: 5:30 AM - 10:30 PM</li>
                                <li>Frecuencia: Cada 20 minutos</li>
                            </ul>
                        </div>

                        <h3>Paradas</h3>
                        <div class="stops-list">
                            <ol>
                                <li>Terminal Oeste - 5:30 AM</li>
                                <li>Parque Industrial - 5:45 AM</li>
                                <li>Centro Financiero - 6:00 AM</li>
                                <li>Hospital Universitario - 6:15 AM</li>
                                <li>Plaza Comercial - 6:25 AM</li>
                                <li>Campus Universitario - 6:40 AM</li>
                            </ol>
                            <p><small>* Los horarios son aproximados y se repiten cada 20 minutos</small></p>
                        </div>
                    </div>

                    <div class="route-media">
                        <h3>Autobús de la Ruta 28</h3>
                        <img src="/api/placeholder/400/250" alt="Autobús de la Ruta 28" class="route-image">

                        <h3>Mapa de la Ruta</h3>
                        <iframe
                            src="https://www.google.com/maps/d/u/1/embed?mid=1V8NZO1XAZciCAw1khnLwbhce89tsVq0&ehbc=2E312F&noprof=1"
                            width="640" height="480"></iframe>
                        </a>
                        <p><small>Haz clic en el mapa para ver la ruta en Google Maps</small></p>
                    </div>
                </div>
            </div>

            <!-- Ruta 4 -->
            <div class="route-card" data-route="28" data-features="wifi,ac"
                data-stops="Terminal Oeste,Parque Industrial,Centro Financiero,Hospital Universitario,Plaza Comercial,Campus Universitario">
                <div class="route-header">
                    Ruta 28 - Oeste a Este
                </div>
                <div class="route-content">
                    <div class="route-info">
                        <h3>Características del Transporte</h3>
                        <div class="bus-features">
                            <ul class="feature-list">
                                <li>WiFi gratuito</li>
                                <li>Aire acondicionado</li>
                                <li>Capacidad para 50 pasajeros</li>
                                <li>Puertos USB para carga de dispositivos</li>
                                <li>Horario: 5:30 AM - 10:30 PM</li>
                                <li>Frecuencia: Cada 20 minutos</li>
                            </ul>
                        </div>

                        <h3>Paradas</h3>
                        <div class="stops-list">
                            <ol>
                                <li>Terminal Oeste - 5:30 AM</li>
                                <li>Parque Industrial - 5:45 AM</li>
                                <li>Centro Financiero - 6:00 AM</li>
                                <li>Hospital Universitario - 6:15 AM</li>
                                <li>Plaza Comercial - 6:25 AM</li>
                                <li>Campus Universitario - 6:40 AM</li>
                            </ol>
                            <p><small>* Los horarios son aproximados y se repiten cada 20 minutos</small></p>
                        </div>
                    </div>

                    <div class="route-media">
                        <h3>Autobús de la Ruta 28</h3>
                        <img src="/api/placeholder/400/250" alt="Autobús de la Ruta 28" class="route-image">

                        <h3>Mapa de la Ruta</h3>
                        <iframe
                            src="https://www.google.com/maps/d/u/1/embed?mid=1s_EW1rbX7DRsd3xmzlR7I-nGkVWhSss&ehbc=2E312F&noprof=1"
                            width="640" height="480"></iframe>
                        </a>
                        <p><small>Haz clic en el mapa para ver la ruta en Google Maps</small></p>
                    </div>
                </div>
            </div>

            <!-- Ruta 5 -->
            <div class="route-card" data-route="28" data-features="wifi,ac"
                data-stops="Terminal Oeste,Parque Industrial,Centro Financiero,Hospital Universitario,Plaza Comercial,Campus Universitario">
                <div class="route-header">
                    Ruta 28 - Oeste a Este
                </div>
                <div class="route-content">
                    <div class="route-info">
                        <h3>Características del Transporte</h3>
                        <div class="bus-features">
                            <ul class="feature-list">
                                <li>WiFi gratuito</li>
                                <li>Aire acondicionado</li>
                                <li>Capacidad para 50 pasajeros</li>
                                <li>Puertos USB para carga de dispositivos</li>
                                <li>Horario: 5:30 AM - 10:30 PM</li>
                                <li>Frecuencia: Cada 20 minutos</li>
                            </ul>
                        </div>

                        <h3>Paradas</h3>
                        <div class="stops-list">
                            <ol>
                                <li>Terminal Oeste - 5:30 AM</li>
                                <li>Parque Industrial - 5:45 AM</li>
                                <li>Centro Financiero - 6:00 AM</li>
                                <li>Hospital Universitario - 6:15 AM</li>
                                <li>Plaza Comercial - 6:25 AM</li>
                                <li>Campus Universitario - 6:40 AM</li>
                            </ol>
                            <p><small>* Los horarios son aproximados y se repiten cada 20 minutos</small></p>
                        </div>
                    </div>

                    <div class="route-media">
                        <h3>Autobús de la Ruta 28</h3>
                        <img src="/api/placeholder/400/250" alt="Autobús de la Ruta 28" class="route-image">

                        <h3>Mapa de la Ruta</h3>
                        <iframe
                            src="https://www.google.com/maps/d/u/1/embed?mid=1HSRSF97diSY87TZF_mXXVkVuaQc_ZDE&ehbc=2E312F&noprof=1"
                            width="640" height="480"></iframe>
                        </a>
                        <p><small>Haz clic en el mapa para ver la ruta en Google Maps</small></p>
                    </div>
                </div>
            </div>
            <!-- Ruta 6 -->
            <div class="route-card" data-route="28" data-features="wifi,ac"
                data-stops="Terminal Oeste,Parque Industrial,Centro Financiero,Hospital Universitario,Plaza Comercial,Campus Universitario">
                <div class="route-header">
                    Ruta 28 - Oeste a Este
                </div>
                <div class="route-content">
                    <div class="route-info">
                        <h3>Características del Transporte</h3>
                        <div class="bus-features">
                            <ul class="feature-list">
                                <li>WiFi gratuito</li>
                                <li>Aire acondicionado</li>
                                <li>Capacidad para 50 pasajeros</li>
                                <li>Puertos USB para carga de dispositivos</li>
                                <li>Horario: 5:30 AM - 10:30 PM</li>
                                <li>Frecuencia: Cada 20 minutos</li>
                            </ul>
                        </div>

                        <h3>Paradas</h3>
                        <div class="stops-list">
                            <ol>
                                <li>Terminal Oeste - 5:30 AM</li>
                                <li>Parque Industrial - 5:45 AM</li>
                                <li>Centro Financiero - 6:00 AM</li>
                                <li>Hospital Universitario - 6:15 AM</li>
                                <li>Plaza Comercial - 6:25 AM</li>
                                <li>Campus Universitario - 6:40 AM</li>
                            </ol>
                            <p><small>* Los horarios son aproximados y se repiten cada 20 minutos</small></p>
                        </div>
                    </div>

                    <div class="route-media">
                        <h3>Autobús de la Ruta 28</h3>
                        <img src="/api/placeholder/400/250" alt="Autobús de la Ruta 28" class="route-image">

                        <h3>Mapa de la Ruta</h3>
                        <iframe
                            src="https://www.google.com/maps/d/u/1/embed?mid=1nXrUuwjF_B2DOo4ja2jk8MR_AqDgw4Q&ehbc=2E312F&noprof=1"
                            width="640" height="480"></iframe>
                        </a>
                        <p><small>Haz clic en el mapa para ver la ruta en Google Maps</small></p>
                    </div>
                </div>
            </div>

            <!-- Ruta 7 -->
            <div class="route-card" data-route="28" data-features="wifi,ac"
                data-stops="Terminal Oeste,Parque Industrial,Centro Financiero,Hospital Universitario,Plaza Comercial,Campus Universitario">
                <div class="route-header">
                    Ruta 28 - Oeste a Este
                </div>
                <div class="route-content">
                    <div class="route-info">
                        <h3>Características del Transporte</h3>
                        <div class="bus-features">
                            <ul class="feature-list">
                                <li>WiFi gratuito</li>
                                <li>Aire acondicionado</li>
                                <li>Capacidad para 50 pasajeros</li>
                                <li>Puertos USB para carga de dispositivos</li>
                                <li>Horario: 5:30 AM - 10:30 PM</li>
                                <li>Frecuencia: Cada 20 minutos</li>
                            </ul>
                        </div>

                        <h3>Paradas</h3>
                        <div class="stops-list">
                            <ol>
                                <li>Terminal Oeste - 5:30 AM</li>
                                <li>Parque Industrial - 5:45 AM</li>
                                <li>Centro Financiero - 6:00 AM</li>
                                <li>Hospital Universitario - 6:15 AM</li>
                                <li>Plaza Comercial - 6:25 AM</li>
                                <li>Campus Universitario - 6:40 AM</li>
                            </ol>
                            <p><small>* Los horarios son aproximados y se repiten cada 20 minutos</small></p>
                        </div>
                    </div>

                    <div class="route-media">
                        <h3>Autobús de la Ruta 28</h3>
                        <img src="/api/placeholder/400/250" alt="Autobús de la Ruta 28" class="route-image">

                        <h3>Mapa de la Ruta</h3>
                        <iframe
                            src="https://www.google.com/maps/d/u/1/embed?mid=1tqTwKX-SOjoS_CFt2v8FGVfLSPohqoM&ehbc=2E312F&noprof=1"
                            width="640" height="480"></iframe>
                        </a>
                        <p><small>Haz clic en el mapa para ver la ruta en Google Maps</small></p>
                    </div>
                </div>
            </div>

            <!-- Ruta 8 -->
            <div class="route-card" data-route="28" data-features="wifi,ac"
                data-stops="Terminal Oeste,Parque Industrial,Centro Financiero,Hospital Universitario,Plaza Comercial,Campus Universitario">
                <div class="route-header">
                    Ruta 28 - Oeste a Este
                </div>
                <div class="route-content">
                    <div class="route-info">
                        <h3>Características del Transporte</h3>
                        <div class="bus-features">
                            <ul class="feature-list">
                                <li>WiFi gratuito</li>
                                <li>Aire acondicionado</li>
                                <li>Capacidad para 50 pasajeros</li>
                                <li>Puertos USB para carga de dispositivos</li>
                                <li>Horario: 5:30 AM - 10:30 PM</li>
                                <li>Frecuencia: Cada 20 minutos</li>
                            </ul>
                        </div>

                        <h3>Paradas</h3>
                        <div class="stops-list">
                            <ol>
                                <li>Terminal Oeste - 5:30 AM</li>
                                <li>Parque Industrial - 5:45 AM</li>
                                <li>Centro Financiero - 6:00 AM</li>
                                <li>Hospital Universitario - 6:15 AM</li>
                                <li>Plaza Comercial - 6:25 AM</li>
                                <li>Campus Universitario - 6:40 AM</li>
                            </ol>
                            <p><small>* Los horarios son aproximados y se repiten cada 20 minutos</small></p>
                        </div>
                    </div>

                    <div class="route-media">
                        <h3>Autobús de la Ruta 28</h3>
                        <img src="/api/placeholder/400/250" alt="Autobús de la Ruta 28" class="route-image">

                        <h3>Mapa de la Ruta</h3>
                        <iframe
                            src="https://www.google.com/maps/d/u/1/embed?mid=1V8NZO1XAZciCAw1khnLwbhce89tsVq0&ehbc=2E312F&noprof=1"
                            width="640" height="480"></iframe>
                        </a>
                        <p><small>Haz clic en el mapa para ver la ruta en Google Maps</small></p>
                    </div>
                </div>
            </div>

            <!-- Ruta 9 -->
            <div class="route-card" data-route="28" data-features="wifi,ac"
                data-stops="Terminal Oeste,Parque Industrial,Centro Financiero,Hospital Universitario,Plaza Comercial,Campus Universitario">
                <div class="route-header">
                    Ruta 28 - Oeste a Este
                </div>
                <div class="route-content">
                    <div class="route-info">
                        <h3>Características del Transporte</h3>
                        <div class="bus-features">
                            <ul class="feature-list">
                                <li>WiFi gratuito</li>
                                <li>Aire acondicionado</li>
                                <li>Capacidad para 50 pasajeros</li>
                                <li>Puertos USB para carga de dispositivos</li>
                                <li>Horario: 5:30 AM - 10:30 PM</li>
                                <li>Frecuencia: Cada 20 minutos</li>
                            </ul>
                        </div>

                        <h3>Paradas</h3>
                        <div class="stops-list">
                            <ol>
                                <li>Terminal Oeste - 5:30 AM</li>
                                <li>Parque Industrial - 5:45 AM</li>
                                <li>Centro Financiero - 6:00 AM</li>
                                <li>Hospital Universitario - 6:15 AM</li>
                                <li>Plaza Comercial - 6:25 AM</li>
                                <li>Campus Universitario - 6:40 AM</li>
                            </ol>
                            <p><small>* Los horarios son aproximados y se repiten cada 20 minutos</small></p>
                        </div>
                    </div>

                    <div class="route-media">
                        <h3>Autobús de la Ruta 28</h3>
                        <img src="/api/placeholder/400/250" alt="Autobús de la Ruta 28" class="route-image">

                        <h3>Mapa de la Ruta</h3>
                        <iframe
                            src="https://www.google.com/maps/d/u/1/embed?mid=1V8NZO1XAZciCAw1khnLwbhce89tsVq0&ehbc=2E312F&noprof=1"
                            width="640" height="480"></iframe>
                        </a>
                        <p><small>Haz clic en el mapa para ver la ruta en Google Maps</small></p>
                    </div>
                </div>
            </div>

            <!-- Ruta 10 -->
            <div class="route-card" data-route="28" data-features="wifi,ac"
                data-stops="Terminal Oeste,Parque Industrial,Centro Financiero,Hospital Universitario,Plaza Comercial,Campus Universitario">
                <div class="route-header">
                    Ruta 28 - Oeste a Este
                </div>
                <div class="route-content">
                    <div class="route-info">
                        <h3>Características del Transporte</h3>
                        <div class="bus-features">
                            <ul class="feature-list">
                                <li>WiFi gratuito</li>
                                <li>Aire acondicionado</li>
                                <li>Capacidad para 50 pasajeros</li>
                                <li>Puertos USB para carga de dispositivos</li>
                                <li>Horario: 5:30 AM - 10:30 PM</li>
                                <li>Frecuencia: Cada 20 minutos</li>
                            </ul>
                        </div>

                        <h3>Paradas</h3>
                        <div class="stops-list">
                            <ol>
                                <li>Terminal Oeste - 5:30 AM</li>
                                <li>Parque Industrial - 5:45 AM</li>
                                <li>Centro Financiero - 6:00 AM</li>
                                <li>Hospital Universitario - 6:15 AM</li>
                                <li>Plaza Comercial - 6:25 AM</li>
                                <li>Campus Universitario - 6:40 AM</li>
                            </ol>
                            <p><small>* Los horarios son aproximados y se repiten cada 20 minutos</small></p>
                        </div>
                    </div>

                    <div class="route-media">
                        <h3>Autobús de la Ruta 28</h3>
                        <img src="/api/placeholder/400/250" alt="Autobús de la Ruta 28" class="route-image">

                        <h3>Mapa de la Ruta</h3>
                        <iframe
                            src="https://www.google.com/maps/d/u/1/embed?mid=1V8NZO1XAZciCAw1khnLwbhce89tsVq0&ehbc=2E312F&noprof=1"
                            width="640" height="480"></iframe>
                        </a>
                        <p><small>Haz clic en el mapa para ver la ruta en Google Maps</small></p>
                    </div>
                </div>
            </div>

            <!-- Ruta 11 -->
            <div class="route-card" data-route="28" data-features="wifi,ac"
                data-stops="Terminal Oeste,Parque Industrial,Centro Financiero,Hospital Universitario,Plaza Comercial,Campus Universitario">
                <div class="route-header">
                    Ruta 28 - Oeste a Este
                </div>
                <div class="route-content">
                    <div class="route-info">
                        <h3>Características del Transporte</h3>
                        <div class="bus-features">
                            <ul class="feature-list">
                                <li>WiFi gratuito</li>
                                <li>Aire acondicionado</li>
                                <li>Capacidad para 50 pasajeros</li>
                                <li>Puertos USB para carga de dispositivos</li>
                                <li>Horario: 5:30 AM - 10:30 PM</li>
                                <li>Frecuencia: Cada 20 minutos</li>
                            </ul>
                        </div>

                        <h3>Paradas</h3>
                        <div class="stops-list">
                            <ol>
                                <li>Terminal Oeste - 5:30 AM</li>
                                <li>Parque Industrial - 5:45 AM</li>
                                <li>Centro Financiero - 6:00 AM</li>
                                <li>Hospital Universitario - 6:15 AM</li>
                                <li>Plaza Comercial - 6:25 AM</li>
                                <li>Campus Universitario - 6:40 AM</li>
                            </ol>
                            <p><small>* Los horarios son aproximados y se repiten cada 20 minutos</small></p>
                        </div>
                    </div>

                    <div class="route-media">
                        <h3>Autobús de la Ruta 28</h3>
                        <img src="/api/placeholder/400/250" alt="Autobús de la Ruta 28" class="route-image">

                        <h3>Mapa de la Ruta</h3>
                        <iframe
                            src="https://www.google.com/maps/d/u/1/embed?mid=1V8NZO1XAZciCAw1khnLwbhce89tsVq0&ehbc=2E312F&noprof=1"
                            width="640" height="480"></iframe>
                        </a>
                        <p><small>Haz clic en el mapa para ver la ruta en Google Maps</small></p>
                    </div>
                </div>
            </div>

            <!-- Ruta 11 -->
            <div class="route-card" data-route="28" data-features="wifi,ac"
                data-stops="Terminal Oeste,Parque Industrial,Centro Financiero,Hospital Universitario,Plaza Comercial,Campus Universitario">
                <div class="route-header">
                    Ruta 28 - Oeste a Este
                </div>
                <div class="route-content">
                    <div class="route-info">
                        <h3>Características del Transporte</h3>
                        <div class="bus-features">
                            <ul class="feature-list">
                                <li>WiFi gratuito</li>
                                <li>Aire acondicionado</li>
                                <li>Capacidad para 50 pasajeros</li>
                                <li>Puertos USB para carga de dispositivos</li>
                                <li>Horario: 5:30 AM - 10:30 PM</li>
                                <li>Frecuencia: Cada 20 minutos</li>
                            </ul>
                        </div>

                        <h3>Paradas</h3>
                        <div class="stops-list">
                            <ol>
                                <li>Terminal Oeste - 5:30 AM</li>
                                <li>Parque Industrial - 5:45 AM</li>
                                <li>Centro Financiero - 6:00 AM</li>
                                <li>Hospital Universitario - 6:15 AM</li>
                                <li>Plaza Comercial - 6:25 AM</li>
                                <li>Campus Universitario - 6:40 AM</li>
                            </ol>
                            <p><small>* Los horarios son aproximados y se repiten cada 20 minutos</small></p>
                        </div>
                    </div>

                    <div class="route-media">
                        <h3>Autobús de la Ruta 28</h3>
                        <img src="/api/placeholder/400/250" alt="Autobús de la Ruta 28" class="route-image">

                        <h3>Mapa de la Ruta</h3>
                        <iframe
                            src="https://www.google.com/maps/d/u/1/embed?mid=1V8NZO1XAZciCAw1khnLwbhce89tsVq0&ehbc=2E312F&noprof=1"
                            width="640" height="480"></iframe>
                        </a>
                        <p><small>Haz clic en el mapa para ver la ruta en Google Maps</small></p>
                    </div>
                </div>
            </div>
            <!-- Ruta 11 -->
            <div class="route-card" data-route="28" data-features="wifi,ac"
                data-stops="Terminal Oeste,Parque Industrial,Centro Financiero,Hospital Universitario,Plaza Comercial,Campus Universitario">
                <div class="route-header">
                    Ruta 28 - Oeste a Este
                </div>
                <div class="route-content">
                    <div class="route-info">
                        <h3>Características del Transporte</h3>
                        <div class="bus-features">
                            <ul class="feature-list">
                                <li>WiFi gratuito</li>
                                <li>Aire acondicionado</li>
                                <li>Capacidad para 50 pasajeros</li>
                                <li>Puertos USB para carga de dispositivos</li>
                                <li>Horario: 5:30 AM - 10:30 PM</li>
                                <li>Frecuencia: Cada 20 minutos</li>
                            </ul>
                        </div>

                        <h3>Paradas</h3>
                        <div class="stops-list">
                            <ol>
                                <li>Terminal Oeste - 5:30 AM</li>
                                <li>Parque Industrial - 5:45 AM</li>
                                <li>Centro Financiero - 6:00 AM</li>
                                <li>Hospital Universitario - 6:15 AM</li>
                                <li>Plaza Comercial - 6:25 AM</li>
                                <li>Campus Universitario - 6:40 AM</li>
                            </ol>
                            <p><small>* Los horarios son aproximados y se repiten cada 20 minutos</small></p>
                        </div>
                    </div>

                    <div class="route-media">
                        <h3>Autobús de la Ruta 28</h3>
                        <img src="/api/placeholder/400/250" alt="Autobús de la Ruta 28" class="route-image">

                        <h3>Mapa de la Ruta</h3>
                        <iframe
                            src="https://www.google.com/maps/d/u/1/embed?mid=1V8NZO1XAZciCAw1khnLwbhce89tsVq0&ehbc=2E312F&noprof=1"
                            width="640" height="480"></iframe>
                        </a>
                        <p><small>Haz clic en el mapa para ver la ruta en Google Maps</small></p>
                    </div>
                </div>
            </div>
            <!-- Ruta 11 -->
            <div class="route-card" data-route="28" data-features="wifi,ac"
                data-stops="Terminal Oeste,Parque Industrial,Centro Financiero,Hospital Universitario,Plaza Comercial,Campus Universitario">
                <div class="route-header">
                    Ruta 28 - Oeste a Este
                </div>
                <div class="route-content">
                    <div class="route-info">
                        <h3>Características del Transporte</h3>
                        <div class="bus-features">
                            <ul class="feature-list">
                                <li>WiFi gratuito</li>
                                <li>Aire acondicionado</li>
                                <li>Capacidad para 50 pasajeros</li>
                                <li>Puertos USB para carga de dispositivos</li>
                                <li>Horario: 5:30 AM - 10:30 PM</li>
                                <li>Frecuencia: Cada 20 minutos</li>
                            </ul>
                        </div>

                        <h3>Paradas</h3>
                        <div class="stops-list">
                            <ol>
                                <li>Terminal Oeste - 5:30 AM</li>
                                <li>Parque Industrial - 5:45 AM</li>
                                <li>Centro Financiero - 6:00 AM</li>
                                <li>Hospital Universitario - 6:15 AM</li>
                                <li>Plaza Comercial - 6:25 AM</li>
                                <li>Campus Universitario - 6:40 AM</li>
                            </ol>
                            <p><small>* Los horarios son aproximados y se repiten cada 20 minutos</small></p>
                        </div>
                    </div>

                    <div class="route-media">
                        <h3>Autobús de la Ruta 28</h3>
                        <img src="/api/placeholder/400/250" alt="Autobús de la Ruta 28" class="route-image">

                        <h3>Mapa de la Ruta</h3>
                        <iframe
                            src="https://www.google.com/maps/d/u/1/embed?mid=1V8NZO1XAZciCAw1khnLwbhce89tsVq0&ehbc=2E312F&noprof=1"
                            width="640" height="480"></iframe>
                        </a>
                        <p><small>Haz clic en el mapa para ver la ruta en Google Maps</small></p>
                    </div>
                </div>
            </div>

            <!-- Ruta 11 -->
            <div class="route-card" data-route="28" data-features="wifi,ac"
                data-stops="Terminal Oeste,Parque Industrial,Centro Financiero,Hospital Universitario,Plaza Comercial,Campus Universitario">
                <div class="route-header">
                    Ruta 28 - Oeste a Este
                </div>
                <div class="route-content">
                    <div class="route-info">
                        <h3>Características del Transporte</h3>
                        <div class="bus-features">
                            <ul class="feature-list">
                                <li>WiFi gratuito</li>
                                <li>Aire acondicionado</li>
                                <li>Capacidad para 50 pasajeros</li>
                                <li>Puertos USB para carga de dispositivos</li>
                                <li>Horario: 5:30 AM - 10:30 PM</li>
                                <li>Frecuencia: Cada 20 minutos</li>
                            </ul>
                        </div>

                        <h3>Paradas</h3>
                        <div class="stops-list">
                            <ol>
                                <li>Terminal Oeste - 5:30 AM</li>
                                <li>Parque Industrial - 5:45 AM</li>
                                <li>Centro Financiero - 6:00 AM</li>
                                <li>Hospital Universitario - 6:15 AM</li>
                                <li>Plaza Comercial - 6:25 AM</li>
                                <li>Campus Universitario - 6:40 AM</li>
                            </ol>
                            <p><small>* Los horarios son aproximados y se repiten cada 20 minutos</small></p>
                        </div>
                    </div>

                    <div class="route-media">
                        <h3>Autobús de la Ruta 28</h3>
                        <img src="/api/placeholder/400/250" alt="Autobús de la Ruta 28" class="route-image">

                        <h3>Mapa de la Ruta</h3>
                        <iframe
                            src="https://www.google.com/maps/d/u/1/embed?mid=1V8NZO1XAZciCAw1khnLwbhce89tsVq0&ehbc=2E312F&noprof=1"
                            width="640" height="480"></iframe>
                        </a>
                        <p><small>Haz clic en el mapa para ver la ruta en Google Maps</small></p>
                    </div>
                </div>
            </div>

            <!-- Ruta 11 -->
            <div class="route-card" data-route="28" data-features="wifi,ac"
                data-stops="Terminal Oeste,Parque Industrial,Centro Financiero,Hospital Universitario,Plaza Comercial,Campus Universitario">
                <div class="route-header">
                    Ruta 28 - Oeste a Este
                </div>
                <div class="route-content">
                    <div class="route-info">
                        <h3>Características del Transporte</h3>
                        <div class="bus-features">
                            <ul class="feature-list">
                                <li>WiFi gratuito</li>
                                <li>Aire acondicionado</li>
                                <li>Capacidad para 50 pasajeros</li>
                                <li>Puertos USB para carga de dispositivos</li>
                                <li>Horario: 5:30 AM - 10:30 PM</li>
                                <li>Frecuencia: Cada 20 minutos</li>
                            </ul>
                        </div>

                        <h3>Paradas</h3>
                        <div class="stops-list">
                            <ol>
                                <li>Terminal Oeste - 5:30 AM</li>
                                <li>Parque Industrial - 5:45 AM</li>
                                <li>Centro Financiero - 6:00 AM</li>
                                <li>Hospital Universitario - 6:15 AM</li>
                                <li>Plaza Comercial - 6:25 AM</li>
                                <li>Campus Universitario - 6:40 AM</li>
                            </ol>
                            <p><small>* Los horarios son aproximados y se repiten cada 20 minutos</small></p>
                        </div>
                    </div>

                    <div class="route-media">
                        <h3>Autobús de la Ruta 28</h3>
                        <img src="/api/placeholder/400/250" alt="Autobús de la Ruta 28" class="route-image">

                        <h3>Mapa de la Ruta</h3>
                        <iframe
                            src="https://www.google.com/maps/d/u/1/embed?mid=1V8NZO1XAZciCAw1khnLwbhce89tsVq0&ehbc=2E312F&noprof=1"
                            width="640" height="480"></iframe>
                        </a>
                        <p><small>Haz clic en el mapa para ver la ruta en Google Maps</small></p>
                    </div>
                </div>
            </div>

            <!-- Ruta 11 -->
            <div class="route-card" data-route="28" data-features="wifi,ac"
                data-stops="Terminal Oeste,Parque Industrial,Centro Financiero,Hospital Universitario,Plaza Comercial,Campus Universitario">
                <div class="route-header">
                    Ruta 28 - Oeste a Este
                </div>
                <div class="route-content">
                    <div class="route-info">
                        <h3>Características del Transporte</h3>
                        <div class="bus-features">
                            <ul class="feature-list">
                                <li>WiFi gratuito</li>
                                <li>Aire acondicionado</li>
                                <li>Capacidad para 50 pasajeros</li>
                                <li>Puertos USB para carga de dispositivos</li>
                                <li>Horario: 5:30 AM - 10:30 PM</li>
                                <li>Frecuencia: Cada 20 minutos</li>
                            </ul>
                        </div>

                        <h3>Paradas</h3>
                        <div class="stops-list">
                            <ol>
                                <li>Terminal Oeste - 5:30 AM</li>
                                <li>Parque Industrial - 5:45 AM</li>
                                <li>Centro Financiero - 6:00 AM</li>
                                <li>Hospital Universitario - 6:15 AM</li>
                                <li>Plaza Comercial - 6:25 AM</li>
                                <li>Campus Universitario - 6:40 AM</li>
                            </ol>
                            <p><small>* Los horarios son aproximados y se repiten cada 20 minutos</small></p>
                        </div>
                    </div>

                    <div class="route-media">
                        <h3>Autobús de la Ruta 28</h3>
                        <img src="/api/placeholder/400/250" alt="Autobús de la Ruta 28" class="route-image">

                        <h3>Mapa de la Ruta</h3>
                        <iframe
                            src="https://www.google.com/maps/d/u/1/embed?mid=1V8NZO1XAZciCAw1khnLwbhce89tsVq0&ehbc=2E312F&noprof=1"
                            width="640" height="480"></iframe>
                        </a>
                        <p><small>Haz clic en el mapa para ver la ruta en Google Maps</small></p>
                    </div>
                </div>
            </div>

            <!-- Ruta 11 -->
            <div class="route-card" data-route="28" data-features="wifi,ac"
                data-stops="Terminal Oeste,Parque Industrial,Centro Financiero,Hospital Universitario,Plaza Comercial,Campus Universitario">
                <div class="route-header">
                    Ruta 28 - Oeste a Este
                </div>
                <div class="route-content">
                    <div class="route-info">
                        <h3>Características del Transporte</h3>
                        <div class="bus-features">
                            <ul class="feature-list">
                                <li>WiFi gratuito</li>
                                <li>Aire acondicionado</li>
                                <li>Capacidad para 50 pasajeros</li>
                                <li>Puertos USB para carga de dispositivos</li>
                                <li>Horario: 5:30 AM - 10:30 PM</li>
                                <li>Frecuencia: Cada 20 minutos</li>
                            </ul>
                        </div>

                        <h3>Paradas</h3>
                        <div class="stops-list">
                            <ol>
                                <li>Terminal Oeste - 5:30 AM</li>
                                <li>Parque Industrial - 5:45 AM</li>
                                <li>Centro Financiero - 6:00 AM</li>
                                <li>Hospital Universitario - 6:15 AM</li>
                                <li>Plaza Comercial - 6:25 AM</li>
                                <li>Campus Universitario - 6:40 AM</li>
                            </ol>
                            <p><small>* Los horarios son aproximados y se repiten cada 20 minutos</small></p>
                        </div>
                    </div>

                    <div class="route-media">
                        <h3>Autobús de la Ruta 28</h3>
                        <img src="/api/placeholder/400/250" alt="Autobús de la Ruta 28" class="route-image">

                        <h3>Mapa de la Ruta</h3>
                        <iframe
                            src="https://www.google.com/maps/d/u/1/embed?mid=1V8NZO1XAZciCAw1khnLwbhce89tsVq0&ehbc=2E312F&noprof=1"
                            width="640" height="480"></iframe>
                        </a>
                        <p><small>Haz clic en el mapa para ver la ruta en Google Maps</small></p>
                    </div>
                </div>
            </div>

            <!-- Ruta 11 -->
            <div class="route-card" data-route="28" data-features="wifi,ac"
                data-stops="Terminal Oeste,Parque Industrial,Centro Financiero,Hospital Universitario,Plaza Comercial,Campus Universitario">
                <div class="route-header">
                    Ruta 28 - Oeste a Este
                </div>
                <div class="route-content">
                    <div class="route-info">
                        <h3>Características del Transporte</h3>
                        <div class="bus-features">
                            <ul class="feature-list">
                                <li>WiFi gratuito</li>
                                <li>Aire acondicionado</li>
                                <li>Capacidad para 50 pasajeros</li>
                                <li>Puertos USB para carga de dispositivos</li>
                                <li>Horario: 5:30 AM - 10:30 PM</li>
                                <li>Frecuencia: Cada 20 minutos</li>
                            </ul>
                        </div>

                        <h3>Paradas</h3>
                        <div class="stops-list">
                            <ol>
                                <li>Terminal Oeste - 5:30 AM</li>
                                <li>Parque Industrial - 5:45 AM</li>
                                <li>Centro Financiero - 6:00 AM</li>
                                <li>Hospital Universitario - 6:15 AM</li>
                                <li>Plaza Comercial - 6:25 AM</li>
                                <li>Campus Universitario - 6:40 AM</li>
                            </ol>
                            <p><small>* Los horarios son aproximados y se repiten cada 20 minutos</small></p>
                        </div>
                    </div>

                    <div class="route-media">
                        <h3>Autobús de la Ruta 28</h3>
                        <img src="/api/placeholder/400/250" alt="Autobús de la Ruta 28" class="route-image">

                        <h3>Mapa de la Ruta</h3>
                        <iframe
                            src="https://www.google.com/maps/d/u/1/embed?mid=1V8NZO1XAZciCAw1khnLwbhce89tsVq0&ehbc=2E312F&noprof=1"
                            width="640" height="480"></iframe>
                        </a>
                        <p><small>Haz clic en el mapa para ver la ruta en Google Maps</small></p>
                    </div>
                </div>
            </div>

            <!-- Ruta 11 -->
            <div class="route-card" data-route="28" data-features="wifi,ac"
                data-stops="Terminal Oeste,Parque Industrial,Centro Financiero,Hospital Universitario,Plaza Comercial,Campus Universitario">
                <div class="route-header">
                    Ruta 28 - Oeste a Este
                </div>
                <div class="route-content">
                    <div class="route-info">
                        <h3>Características del Transporte</h3>
                        <div class="bus-features">
                            <ul class="feature-list">
                                <li>WiFi gratuito</li>
                                <li>Aire acondicionado</li>
                                <li>Capacidad para 50 pasajeros</li>
                                <li>Puertos USB para carga de dispositivos</li>
                                <li>Horario: 5:30 AM - 10:30 PM</li>
                                <li>Frecuencia: Cada 20 minutos</li>
                            </ul>
                        </div>

                        <h3>Paradas</h3>
                        <div class="stops-list">
                            <ol>
                                <li>Terminal Oeste - 5:30 AM</li>
                                <li>Parque Industrial - 5:45 AM</li>
                                <li>Centro Financiero - 6:00 AM</li>
                                <li>Hospital Universitario - 6:15 AM</li>
                                <li>Plaza Comercial - 6:25 AM</li>
                                <li>Campus Universitario - 6:40 AM</li>
                            </ol>
                            <p><small>* Los horarios son aproximados y se repiten cada 20 minutos</small></p>
                        </div>
                    </div>

                    <div class="route-media">
                        <h3>Autobús de la Ruta 28</h3>
                        <img src="/api/placeholder/400/250" alt="Autobús de la Ruta 28" class="route-image">

                        <h3>Mapa de la Ruta</h3>
                        <iframe
                            src="https://www.google.com/maps/d/u/1/embed?mid=1V8NZO1XAZciCAw1khnLwbhce89tsVq0&ehbc=2E312F&noprof=1"
                            width="640" height="480"></iframe>
                        </a>
                        <p><small>Haz clic en el mapa para ver la ruta en Google Maps</small></p>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <footer>
        <p>©️ 2025 RutasFácil - Tu guía de transporte público</p>
        <p>Contacto: info@rutasfacil.com | Tel: 123-456-7890</p>
    </footer>

    <script>
        // Función de búsqueda
        document.addEventListener('DOMContentLoaded', function () {
            const searchInput = document.getElementById('search-input');
            const searchButton = document.getElementById('search-button');
            const routesContainer = document.getElementById('routes-container');
            const routeCards = document.querySelectorAll('.route-card');
            const navLinks = document.querySelectorAll('nav a');

            // Función para buscar
            function performSearch() {
                const searchTerm = searchInput.value.toLowerCase().trim();
                let resultsFound = false;

                // Obtener filtros seleccionados
                const filterAccesible = document.getElementById('filter-accesible').checked;
                const filterWifi = document.getElementById('filter-wifi').checked;
                const filterAC = document.getElementById('filter-ac').checked;
                const filterEco = document.getElementById('filter-eco').checked;

                routeCards.forEach(card => {
                    // Obtener datos de la tarjeta
                    const routeNumber = card.getAttribute('data-route');
                    const routeHeader = card.querySelector('.route-header').innerText.toLowerCase();
                    const routeStops = card.getAttribute('data-stops').toLowerCase();
                    const routeFeatures = card.getAttribute('data-features').split(',');

                    // Verificar si cumple con los filtros
                    let passFilters = true;
                    if (filterAccesible && !routeFeatures.includes('accesible')) passFilters = false;
                    if (filterWifi && !routeFeatures.includes('wifi')) passFilters = false;
                    if (filterAC && !routeFeatures.includes('ac')) passFilters = false;
                    if (filterEco && !routeFeatures.includes('eco')) passFilters = false;

                    // Verificar texto de búsqueda
                    const matchesSearch = searchTerm === '' ||
                        routeHeader.includes(searchTerm) ||
                        routeNumber.includes(searchTerm) ||
                        routeStops.includes(searchTerm);

                    if (matchesSearch && passFilters) {
                        card.style.display = 'block';
                        resultsFound = true;

                        // Resaltar términos de búsqueda si hay algo buscado
                        if (searchTerm !== '') {
                            highlightSearchTerm(card, searchTerm);
                        } else {
                            // Eliminar resaltados anteriores
                            removeHighlights(card);
                        }
                    } else {
                        card.style.display = 'none';
                    }
                });

                // Mostrar mensaje si no hay resultados
                const noResultsElement = document.querySelector('.no-results');
                if (!resultsFound) {
                    if (!noResultsElement) {
                        const noResults = document.createElement('div');
                        noResults.className = 'no-results';
                        noResults.innerHTML = `
                            <h3>No se encontraron resultados</h3>
                            <p>Intenta con otros términos de búsqueda o ajusta los filtros.</p>
                        `;
                        routesContainer.appendChild(noResults);
                    }
                } else if (noResultsElement) {
                    noResultsElement.remove();
                }
            }

            // Función para resaltar términos de búsqueda
            function highlightSearchTerm(card, term) {
                // Primero eliminar resaltados anteriores
                removeHighlights(card);

                // Función para resaltar texto
                function highlightText(element) {
                    if (element.nodeType === 3) { // Nodo de texto
                        const text = element.nodeValue;
                        const lowerText = text.toLowerCase();
                        if (lowerText.includes(term)) {
                            const container = document.createElement('span');
                            let lastIdx = 0;
                            let idx;

                            while ((idx = lowerText.indexOf(term, lastIdx)) !== -1) {
                                container.appendChild(document.createTextNode(text.substring(lastIdx, idx)));

                                const highlight = document.createElement('span');
                                highlight.className = 'highlight';
                                highlight.appendChild(document.createTextNode(text.substring(idx, idx + term.length)));
                                container.appendChild(highlight);

                                lastIdx = idx + term.length;
                            }

                            if (lastIdx < text.length) {
                                container.appendChild(document.createTextNode(text.substring(lastIdx)));
                            }

                            element.parentNode.replaceChild(container, element);
                        }
                    } else if (element.nodeType === 1 &&
                        !['script', 'style', 'iframe', 'canvas', 'img', 'input', 'textarea'].includes(element.tagName.toLowerCase())) {
                        Array.from(element.childNodes).forEach(child => highlightText(child));
                    }
                }

                // Resaltar en el encabezado
                highlightText(card.querySelector('.route-header'));

                // Resaltar en las paradas
                const stopsList = card.querySelector('.stops-list');
                if (stopsList) {
                    highlightText(stopsList);
                }
            }

            // Función para eliminar resaltados
            function removeHighlights(element) {
                const highlights = element.querySelectorAll('.highlight');
                highlights.forEach(highlight => {
                    const parent = highlight.parentNode;
                    const text = highlight.textContent;
                    const textNode = document.createTextNode(text);
                    parent.replaceChild(textNode, highlight);
                    parent.normalize();
                });
            }

            // Eventos
            searchButton.addEventListener('click', performSearch);
            searchInput.addEventListener('keypress', function (e) {
                if (e.key === 'Enter') {
                    performSearch();
                }
            });

            // Filtros
            const filterCheckboxes = document.querySelectorAll('.filter-checkbox input');
            filterCheckboxes.forEach(checkbox => {
                checkbox.addEventListener('change', performSearch);
            });
