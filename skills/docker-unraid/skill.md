\---

name: docker-unraid

description: À utiliser pour tout projet Docker destiné à Unraid, avec volumes persistants, variables d'environnement, logs clairs, healthcheck et PUID/PGID si pertinent.

\---



Quand ce skill est utilisé :



\- privilégier une configuration par variables d'environnement ;

\- prévoir des volumes persistants explicites ;

\- documenter les chemins Unraid attendus ;

\- ajouter un healthcheck si le service tourne en continu ;

\- prévoir PUID/PGID quand le conteneur écrit dans des volumes ;

\- éviter les permissions root inutiles ;

\- fournir un exemple docker-compose.yml ou paramètres Unraid si demandé.

