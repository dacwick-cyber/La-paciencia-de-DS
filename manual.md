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

