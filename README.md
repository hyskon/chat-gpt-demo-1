# chat-gpt-demo-1
Deze webapp is een chatbot die gebruikers in staat stelt om met een bot te communiceren.

## Afbeeldingen importeren
Het importeert twee afbeeldingen, een voor de bot en een voor de gebruiker.

## Frontend
Er wordt ook een functie genaamd loader gemaakt die wordt gebruikt om te laden wanneer de bot antwoordt. Er is ook een functie genaamd typeText die wordt gebruikt om het antwoord van de bot te typen. Er is ook een functie genaamd generateUniqueId die wordt gebruikt om unieke ID's te maken voor elk bericht dat door de chatbot wordt verzonden. De laatste functie is chatStripe, die wordt gebruikt om hetzelfde bericht in hetzelfde formaat weer te geven als alle andere berichten in de chatroom. 

### HandleSubmit-functie 
De handleSubmit-functie verzendt het bericht naar de server en ontvangt vervolgens corresponerend antwoord van de server. Als alles goed gaat, zal typeText het antwoord typen en anders zal er een foutmelding verschijnen.

## Backend
Deze code maakt gebruik van de OpenAI API om een chatbot te maken.

### Dependencies
De volgende dependencies worden gebruikt: 
- express: Een web framework voor Node.js. 
- dotenv: Een module die het mogelijk maakt om environment variabelen in een .env bestand te laden. 
- cors: Een module die Cross-Origin Resource Sharing (CORS) mogelijk maakt. 
- openai: De OpenAI API module. 

### Configuratie 
De configuratie wordt ingesteld met behulp van de `Configuration` class uit de `openai` module. Hierbij wordt de API key uit het .env bestand gebruikt. 

### Express server 
Vervolgens wordt er een Express server aangemaakt met behulp van `express()`. Daarnaast worden ook CORS en JSON ondersteuning toegevoegd aan de server.  

### Routes 
Er zijn twee routes beschikbaar, namelijk `/` en `/post`. De `/` route stuurt een bericht terug naar de client met daarin "Hallo, bot hier..". De `/post` route verwerkt het bericht dat door de client is gestuurd en stuurt vervolgens een antwoord terug naar de client met daarin het antwoord van de chatbot.
