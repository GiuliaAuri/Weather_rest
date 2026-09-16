# Weather Rest
Applicazione desktop sviluppata in Java e JavaFX per la consultazione delle condizioni meteorologiche e delle previsioni di una città tramite le API OpenWeatherMap. Progetto realizzato per i corsi di Ingegneria del Software e Programmazione a Oggetti, a.a. 2023/2024.

Il progetto utilizza le API di **OpenWeatherMap** per ottenere:

- le coordinate geografiche della città cercata;
- le condizioni meteorologiche attuali;
- la temperatura minima e massima;
- la descrizione del tempo;
- l'umidità;
- la velocità del vento;
- le previsioni delle ore successive.

L'interfaccia grafica modifica dinamicamente icone e sfondo in base alle condizioni meteorologiche rilevate.

## Funzionalità principali

- Ricerca del meteo tramite il nome di una città.
- Conversione del nome della città in coordinate geografiche.
- Recupero dei dati meteorologici tramite API REST.
- Visualizzazione delle condizioni meteo correnti.
- Visualizzazione delle previsioni successive in una tabella.
- Visualizzazione di icone e immagini di sfondo personalizzate.
- Gestione degli errori relativi alla ricerca e alle richieste API.
- Validazione del testo inserito dall'utente.
- Animazioni grafiche dell'interfaccia.

## Tecnologie utilizzate

- **Java 21**
- **JavaFX 21**
- **Maven**
- **OpenWeatherMap API**
- **OkHttp** per le richieste HTTP
- **Jackson** per l'elaborazione delle risposte JSON
- **dotenv-java** per la gestione della chiave API
- **JUnit** per i test
- **AnimateFX** per le animazioni dell'interfaccia
- **FXML** e **CSS** per la struttura e lo stile dell'interfaccia

## Struttura del progetto

```text
Weather_rest/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   ├── com/weather_app/
│   │   │   │   ├── Controller.java
│   │   │   │   ├── WeatherApp.java
│   │   │   │   ├── model/
│   │   │   │   └── rest/
│   │   │   └── module-info.java
│   │   └── resources/
│   │       └── com/weather_app/
│   │           ├── weather-view.fxml
│   │           ├── styles.css
│   │           ├── icon.png
│   │           └── img/
│   └── test/
├── pom.xml
├── .env
└── tesina_ing_del_software.pdf
```

## Prerequisiti

Per eseguire il progetto sono necessari:

- JDK 21 o versione compatibile;
- Maven, oppure il Maven Wrapper incluso nel progetto;
- una chiave API gratuita di OpenWeatherMap.

## Configurazione della chiave API

Creare o modificare il file `.env` nella directory principale del progetto e inserire:

```env
API_KEY=la_tua_chiave_api
```

La chiave API non dovrebbe essere pubblicata su repository accessibili pubblicamente.

## Esecuzione del progetto

Su Linux o macOS:

```bash
./mvnw clean javafx:run
```

Su Windows:

```bash
mvnw.cmd clean javafx:run
```

In alternativa, se Maven è installato sul sistema:

```bash
mvn clean javafx:run
```

## Esecuzione dei test

Per eseguire i test automatici:

```bash
./mvnw test
```

Su Windows:

```bash
mvnw.cmd test
```

## Architettura

Il progetto è organizzato principalmente nei seguenti componenti:

- **Controller**: gestisce gli eventi dell'interfaccia grafica e aggiorna i dati visualizzati.
- **Model**: contiene le classi che rappresentano i dati meteorologici e le coordinate geografiche.
- **REST**: gestisce le richieste HTTP verso i servizi OpenWeatherMap.
- **FXML**: definisce la struttura dell'interfaccia grafica.
- **CSS**: definisce lo stile dell'applicazione.
- **Resources**: contiene icone e immagini associate alle condizioni meteorologiche.

## Licenza

Questo progetto è stato realizzato per finalità didattiche nell'ambito dei corsi universitari di Ingegneria del Software e Programmazione a Oggetti.
