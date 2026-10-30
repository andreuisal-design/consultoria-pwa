CONSULTORIA — ENTREVISTA INICIAL
Versió 0.1 · Pilot edifici d'apartaments

CONTINGUT
- Aplicació web progressiva (PWA) per a entrevista i presa de requeriments.
- Interfície responsive per ordinador, tauleta i mòbil.
- Desa automàticament les respostes al navegador d'aquest dispositiu.
- Pot funcionar offline després de la primera càrrega des d'un servidor HTTP.
- Exporta una còpia JSON de les respostes.
- Genera un resum imprimible / PDF mitjançant el diàleg d'impressió del navegador.

PROVA RÀPIDA A WINDOWS
1. Descomprimeix tota la carpeta.
2. Fes doble clic a INICIAR-WINDOWS.bat.
3. S'obrirà http://localhost:8765 al navegador.
4. Per instal·lar-la com a aplicació, obre el menú del navegador i selecciona
   "Instal·la aquesta aplicació" o "Instal·la Consultoria", si està disponible.
5. Mantén la finestra del terminal oberta mentre utilitzis l'aplicació.

REQUISIT WINDOWS
El fitxer BAT necessita Python 3 instal·lat i accessible. No necessita permisos
d'administrador. Si el PC corporatiu no té Python, es pot publicar al NAS amb Docker
o utilitzar un servidor local ja autoritzat.

INSTAL·LACIÓ A MAC
Amb Terminal, entra a la carpeta descomprimida i executa:
  python3 -m http.server 8765
Després obre http://localhost:8765.

INSTAL·LACIÓ AL NAS (NO EXECUTAR ENCARA)
Es pot publicar aquesta carpeta darrere del servei web del NAS o d'un contenidor
web estàtic. Abans cal decidir autenticació, còpies de seguretat i accés de xarxa.
No s'ha d'exposar a Internet sense protecció.

DADES I LIMITACIONS DE LA V0.1
- Les dades s'emmagatzemen a localStorage del navegador i només en aquell perfil
  i dispositiu. No hi ha sincronització amb el NAS en aquesta versió.
- Exporta periòdicament el JSON amb el botó "Exportar dades".
- No es recomana introduir dades personals sensibles.
- No hi ha encara gestió multiusuari, permisos, càrrega de documents ni sincronització.
- No esborres les dades del navegador abans d'haver exportat una còpia.
- L'estil i la navegació segueixen la línia visual del web Auditor Electricitat existent.

SEGÜENT VERSIÓ
1. Importar/exportar còpies JSON des de la interfície.
2. Desar entrevistes com a registres identificats per client i diagnòstic.
3. Generar checklist de documentació pendent.
4. Afegir formulari específic del taller mecànic reutilitzant el mateix motor.
5. Integrar API i sincronització controlada amb el NAS.
