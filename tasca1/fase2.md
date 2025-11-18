**Fase 2: Treball per parelles**

Treballant per parelles:

1\.       Discussió i Consens: Comparen les seves respostes individuals (Fase 1).

2\.     Elaboració d'una Proposta Unificada: Heu de consensuar i dissenyar el vostre propi Esquema 3-2-1 de Còpies (3 còpies, 2 mitjans, 1 fora de lloc) basat en els requisits del cas.

Parella Marti i Marc

| Element | Proposta de la Parella | Justificació |
| :---- | :---- | :---- |
| Dades Crítiques | **Bases de dades del servidor  i configuracions.**  |  **Les bases de dades són les més sensibles i informació privada els clients es poden restaurar amb imatge estàndard.** |
| Periodicitat (BD) | **Incremental cada 4 hores i una completa setmanal.** |  **Les bases de dades necessiten còpies cada cert temps per no perdre informació així tens copies.** |
| Tipus de Còpia (BD) | **Incremental per  cada 4h, Diferencial per la setmanal, Completa per la mensual.** | **és molt més ràpida i bona de temps i sobretot molta seguretat, et dona restauració total.** |
| Mitjà 1 (Local) | **NAS intern** |  **volem que sigui xarxa, i ajuda a tenir restauracions rapides** |
| Mitjà 2 (Extern) | **Cloud i un disc dur extern**  | **Posem cloud mes un disc extern que protegeix contra desastres físics i té regla 3-2-1 amb còpia fora de l’empresa.** |

Part en parelles Guillem i Miquel

| Element | Proposta de la Parella | Justificació |
| :---- | :---- | :---- |
| Dades Crítiques | Les dades més crítiques del servidor que s’han de prioritzar són les que poden comprometre la informació sensible de l’empresa i dels seus clients. Destaquen especialment les Bases de Dades de comptabilitat i de clients, així com dades de projectes i informació interna. No és necessari copiar completament els 10 equips dels clients, però sí assegurar tota la informació realment important per evitar riscos en cas de pèrdua. |  Hem seleccionat aquestes dades perquè la seva pèrdua podria afectar greument l’empresa i els seus clients. Les Bases de Dades i la informació interna són essencials per al funcionament del negoci. En canvi, els equips dels clients sovint contenen dades menys rellevants; per això, centrar la còpia en la informació crítica permet protegir el que és essencial i optimitzar recursos. |
| Periodicitat (BD) |  Diàriament aplicaríem una còpia de seguretat incremental, ja que és la més ràpida i eficient per fer còpies cada dia. Setmanalment realitzaríem una còpia diferencial, que permet registrar totes les dades modificades des de l’última còpia completa. Finalment, un cop al mes faríem una còpia completa per tenir un punt de restauració total i recent de totes les dades. |  La còpia incremental és la millor opció diària perquè consumeix pocs recursos i és ràpida d’executar, tot i que la recuperació posterior sigui més lenta. La còpia diferencial setmanal permet tenir un volum de dades intermig i una recuperació més senzilla en cas de problema. La còpia completa mensual és necessària per mantenir un estat global i fiable de totes les dades, i el seu impacte en recursos és assumible en fer-la només un cop al mes. |
| Tipus de Còpia (BD) |  El tipus de còpia que utilitzaríem seria el següent: **incremental** per a les còpies diàries, **diferencial** per a les setmanals i **completa** per a la còpia mensual. |  Aquesta combinació permet aconseguir un equilibri entre velocitat, consum de recursos i seguretat de les dades. La incremental és ràpida i ideal per a l’ús diari; la diferencial facilita una recuperació més àgil en comparació amb l’incremental; i la completa assegura un punt de restauració total imprescindible per a la protecció a llarg termini de les Bases de Dades. |
| Mitjà 1 (Local) | Disc dur extern o NAS | Permet tenir la còpia més recent de manera ràpida i accessible. Ideal per restauracions immediates i per mantenir una còpia local segons la regla 3-2-1. |
| Mitjà 2 (Extern) | Còpia al núvol (Cloud) | Garanteix tenir una còpia fora de les instal·lacions. Protegeix davant robatoris, incendis o altres desastres locals i compleix el requisit “off-site” de la regla 3-2-1. |



