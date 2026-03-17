Flujo de trabajo desde el inicio
Crear proyecto desde cero  - camino 1
Mkdir  ‘La paciencia de DS’	(crea directorio)
Ls -la				(verificar que se creó)
drwxr-xr-x 2 dacwi dacwi 4096 Mar 10 13:53 'La paciencia de DS'
Ahora se copiará un archivo de Word para incluir en el directorio La paciencia de DS
explorer.exe . 	(abre una ventana de Windows en la carpeta actual de WSL . Después se copia y/o arrastra)
Con el archivo cargado en Linux, se procede a crear el repositorio en Git
git init	Iniciar el seguimiento de Git
ls -la           	 # Vas a ver una carpeta .git nueva
git status        	# Te va a decir: "hay un archivo sin seguimiento"
El Directorio no tiene README, por lo tanto es conveniente crear uno.
echo "# La paciencia de DS" > README.md
echo "Apuntes y prácticas con mi rock educator" >> README.md
git status			mostrara dos archivos creados en rojo, sin seguimiento
git add .			se solicita a git que rastree todos los archivos creados
git status			mostrará los mismos archivos en verde, rastreado
Se guardaran en Git los archivos preparados y rastreados
git commit -m "Primer commit: apuntes con DS"
git status			# Debería decir: "nothing to commit, working tree clean"
gh repo create "La-paciencia-de-DS" --public --source=. --remote=origin –push
Verificar en el navegador
https://github.com/dacwick-cyber/La-paciencia-de-DS


Agregar archivos a un repositorio ya creado
===========================================
1- Entrar al repositorio
   cd 'La paciencia de DS'

2- Crear el archivo
   nano Manual.md

3- Pegar contenido
   - copiar el texto creado
   - pegar con click derecho
   - guardar con Enter
   - salir con Ctrl+X

4- Verificarlo
   cat Manual.md

5- Agregar a Git
   git add Manual.md
   git commit -m "agrego manual de procedimiento DS"
   git push

6- Verificar en el navegador
   https://github.com/dacwick-cyber/La-paciencia-de-DS



Agregar archivos a un repositorio ya creado - Camino 2 (VERSIÓN COMPLETA)
==========================================================================

[PASO 0 - SOLO SI EL REPO NO EXISTE EN GITHUB]
------------------------------------------------
1. En el navegador, ir a: https://github.com/new
2. Nombre del repositorio: (ej: La-paciencia-de-DS)
3. NO marcar "Add a README"
4. Crear repositorio
5. Copiar la URL que aparece (ej: https://github.com/dacwick-cyber/La-paciencia-de-DS.git)
6. En la terminal, conectar el repo local:
   git remote add origin https://github.com/dacwick-cyber/La-paciencia-de-DS.git
   git branch -M main
   git push -u origin main

[PASOS 1 a 5 - CUANDO EL REPO YA EXISTE EN GITHUB]
---------------------------------------------------
1- Entrar al repositorio local
   cd 'La paciencia de DS'

2- Crear el archivo
   nano Manual.md
   - pegar contenido (click derecho)
   - guardar: Ctrl+O → Enter
   - salir: Ctrl+X

3- Verificar que se creó
   cat Manual.md

4- Agregar a Git
   git add Manual.md
   git status            # opcional: verifica que está en verde
   git commit -m "Agrego manual de procedimiento DS"
   git push              # o git push -u origin main si es primera vez

5- Verificar en el navegador
   https://github.com/dacwick-cyber/La-paciencia-de-DS
