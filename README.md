[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/Giorgio866/Trackerpizzav1/main/Trackerpizzav1.yaml)



# Trackerpizzav1
Automazione homeassistant
Questo Blueprint unifica in un'unica automazione tutta la gestione delle consegne, includendo:
​Monitoraggio Viaggio: Calcola tempi di viaggio, soste e chilometri.
​Notifiche Intelligenti: Avvisa su Telegram e Alexa (annunci vocali).
​Gestione GPS: Attiva automaticamente il GPS "Alta Precisione" a inizio turno (18:00) e lo spegne a fine turno (23:30).
​Rientro in Sede: Avvisa vocalmente quando la Panda torna in pizzeria.
​⚙️ Prerequisiti
​Assicurati di avere in Home Assistant i seguenti Aiutanti (Helpers). Se li hai già dalle vecchie automazioni, puoi riutilizzarli.
​input_datetime.panda_orario_partenza (Orario)
​input_datetime.panda_orario_arrivo (Orario)
​input_number.panda_tempo_viaggio_minuti (Numero)
​input_boolean.panda_in_consegna (Booleano/Toggle)
​counter.contatore_consegne_panda (Contatore Giornaliero)
​counter.panda_consegne_settimanali (Contatore Settimanale)
​counter.panda_consegne_parziali (Contatore per gli annunci Alexa)
​🚀 Installazione
​Copia il file panda_manager_giorgio.yaml nella cartella /config/blueprints/automation/ del tuo Home Assistant.
​Vai su Impostazioni > Automazioni > Crea automazione > Seleziona Blueprint.
​Seleziona "Gestione Completa Panda (Giorgio)".
​Compila i campi:
​Tracker: Il dispositivo GPS (es. device_tracker.panda).
​Notifica App Mobile: Il servizio notify del telefono che sta in auto (es. notify.mobile_app_panda) per comandare il GPS.
​Zona Pizzeria: La tua zona base.
​Alexa: Seleziona gli Echo per gli annunci.
​Telegram Chat ID: 
​Collega tutti gli Helpers creati al punto precedente.
