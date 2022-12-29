 # OpenAI API
Deze code maakt gebruik van de OpenAI API om een chatbot te maken.

## Dependencies
De volgende dependencies worden gebruikt: 
- express: Een web framework voor Node.js. 
- dotenv: Een module die het mogelijk maakt om environment variabelen in een .env bestand te laden. 
- cors: Een module die Cross-Origin Resource Sharing (CORS) mogelijk maakt. 
- openai: De OpenAI API module. 

## Configuratie 
De configuratie wordt ingesteld met behulp van de `Configuration` class uit de `openai` module. Hierbij wordt de API key uit het .env bestand gebruikt. 

## Express server 
Vervolgens wordt er een Express server aangemaakt met behulp van `express()`. Daarnaast worden ook CORS en JSON ondersteuning toegevoegd aan de server.  

## Routes 
Er zijn twee routes beschikbaar, namelijk `/` en `/post`. De `/` route stuurt een bericht terug naar de client met daarin "Hallo, bot hier..". De `/post` route verwerkt het bericht dat door de client is gestuurd en stuurt vervolgens een antwoord terug naar de client met daarin het antwoord van de chatbot.
