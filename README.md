# Rouletterboxd

Ruleta para decidir qué película ver de mi watchlist de Letterboxd.

## Sincronizar entre dispositivos

Lo que quitas («Ya la vi, quitar») y las últimas 8 tiradas se guardan en `estado.json` de este repo, así que se ven igual en el móvil y en el ordenador. Para poder escribir, cada dispositivo necesita un token de GitHub, que se pega una vez en **Ajustes** y solo se guarda en ese navegador:

1. GitHub → **Settings → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token**.
2. **Repository access**: *Only select repositories* → `rouletterboxd`.
3. **Permissions → Repository permissions → Contents**: *Read and write*.
4. Copia el token y pégalo en la ruleta, en **Ajustes → Guardar token**.

Sin token la página funciona igual, pero lo que quites se queda en ese dispositivo. Cada quitada y cada tirada es un commit en el repo.

## Actualizar la lista

1. En Letterboxd: **Settings → Data → Export your data**.
2. Descomprime el zip y busca `watchlist.csv`.
3. En la ruleta, **Ajustes → Subir watchlist.csv** (con el token guardado). También puedes subirlo a mano en GitHub con **Add file → Upload files**.

## Probar en local

Abrir `index.html` con doble clic usa la copia de respaldo que va dentro del HTML. Para que lea `watchlist.csv` hace falta servirlo:

```
python -m http.server
```

y abrir http://localhost:8000.
