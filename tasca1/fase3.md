**Fase 3: Treball en grup**

1\.  Debat i Selecció: Cada parella presenta el seu esquema. El grup debat els pros i contres de cada proposta (cost, temps de recuperació, seguretat, simplicitat).

| Tipus de Dades | Categoria | Freqüència | Tipus de Còpia |
| ----- | ----- | ----- | ----- |
| **Servidor: Bases de Dades Crítiques** (comptabilitat, clients) | Crítica | Cada 4 hores (incremental) i setmanal (diferencial), mensual (completa) | Incremental, Diferencial, Completa |
| **Servidor: Configuracions Crítiques** | Crítica | Setmanal (diferencial), mensual (completa) | Diferencial, Completa |
| **Clients: Dades Crítiques de projectes i informació interna** | Crítica | Diària (incremental), setmanal (diferencial), mensual (completa) | Incremental, Diferencial, Completa |
| **Clients: Dades no crítiques** | No crítica | Setmanal (incremental), mensual (completa) | Incremental, Completa |

2\.    Disseny de la Política Final: El grup ha de redactar la Política de Còpies de Seguretat Definitiva que presentaran a l'empresa "Muntatges i Serveis Tècnics SL".

**Document Final (Fase 3\)**

El grup ha de generar un document amb els següents punts resolts:

1\)      Dades Objecte de Còpia

Quines dades es copien i amb quina freqüència (separant Servidor/Clients i crítiques/no crítiques).

2\)      Cronograma Setmanal Detallat

| Dia | Dades | Tipus de còpia | Mitjà |
| :---- | ----- | ----- | :---- |
| Dilluns | Bases de dades i configuracions crítiques | Incremental | NAS / Disc dur extern |
| Dimarts | Bases de dades i configuracions crítiques | Incremental | NAS / Disc dur extern |
| Dimecres | Bases de dades i configuracions crítiques | Incremental | NAS / Disc dur extern |
| Dijous | Bases de dades i configuracions crítiques | Incremental | NAS / Disc dur extern |
| Divendres | Bases de dades i configuracions crítiques | Incremental | NAS / Disc dur extern |
| Dissabte | Còpia diferencial setmanal de BD i dades crítiques clients | Diferencial | NAS / Disc dur extern \+ Cloud |
| Diumenge | Còpia completa mensual (si toca) de tota la informació crítica | Completa | Cloud / Cinta LTO |

 

3\)      Elecció de Mitjans i Ubicació (Regla 3-2-1)

| Element | Mitjà | Ubicació / Responsable | Justificació |
| ----- | ----- | ----- | ----- |
| **Mitjà 1 (Local)** | NAS intern o Disc dur extern | Instal·lacions de l’empresa, gestionat pel departament IT | Permet restauracions ràpides de la còpia més recent, assegurant disponibilitat immediata. |
| **Mitjà 2 (Extern)** | Cloud (Azure / Google Cloud) \+ Disc dur extern fora del lloc | Ubicació remota o proveïdor de cloud; responsable: IT | Garanteix còpia fora de lloc, protecció davant robatoris, incendis o desastres locals. Compliment de la regla 3-2-1. |
| **Ubicació Fora de Lloc** | Cloud / Disc dur extern en lloc remot | Proveïdor cloud o emmagatzematge físic extern | Manté la còpia off-site, assegurant redundància i seguretat extra de dades crítiques. |

4\)      Estratègia de Recuperació (RTO/RPO)

Com es garanteix que les dades de Comptabilitat/Clients compleixen amb el requisit de RPO (4 hores) i RTO (4 hores).

| Tipus de Dades | RPO (Recovery Point Objective) | RTO (Recovery Time Objective) | Estratègia |
| ----- | ----- | ----- | ----- |
| Bases de dades crítiques i comptabilitat | 4 hores | 4 hores | Les còpies incrementals cada 4 hores garanteixen el mínim de pèrdua de dades (RPO). Restauració ràpida des de NAS o disc dur extern compleix l’RTO. |
| Configuracions i dades crítiques clients | 24 hores | 4 hores | Còpies setmanals i cloud permeten restauració completa en cas de desastre, assegurant disponibilitat segons els requisits de l’empresa. |
| Dades no crítiques | 7 dies | 24-48 hores | Còpies setmanals i mensuals, prioritzant eficiència de recursos i protecció bàsica. |

