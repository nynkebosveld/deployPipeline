# Name three components of your solution, explain what they are and how they relate to each other. A 'component' can be anything from GitHub Actions or Bash to Digital Ocean and SSH.

We gebruiken GitHub actions om een .yml script uit te voeren op het moment dat er gepusht word, Dit wordt vaak gebruikt in CD/CI om het deploy stuk te automatiseren
    De GitHub actions verbindt via een ander vis SSH met de VPS en voert hier het bash script uit om te herstarten. Op het moment dat er gepushed wordt voeren wij via actions/setup-python@v3 een command uit om alle dependecys te downloaden, daar na voeren wij pytest uit pas als die voltooid is gaan we verder. 

# Discuss three problems that you encountered along the way and how you solved them.

1.	Ik had problemen met het verbinden met de SSH. Na wat google werk heb ik het probleem weten op te lossen door een bestaand script te gebruiken. Ik heb dit script de parameters van de VPs meegegeven en toen is het gelukt. 
2.	Ik had problemen met het restarten van de website waardoor hij de veranderingen niet doorzetten. Dit heb ik opgelost door via bash een restart script te schrijven. 
3.	Het laatste “grote” probleem dat ik had was met de pytest. Deze runt op 3.11 maar python runt op 3.9.8. Hierdoor werkten het niet. Ik ben toen op google gaan opzoeken hoe ik dit kon oplossen. Ik heb uiteindelijk via stackoverflow de oplossing gevonden. 
