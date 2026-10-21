# Rouletterboxd

Ruleta para decidir qué película ver de mi watchlist de Letterboxd.

## Actualizar la lista

1. En Letterboxd: **Settings → Data → Export your data**.
2. Descomprime el zip y busca `watchlist.csv`.
3. En este repo en GitHub: **Add file → Upload files**, arrastra el `watchlist.csv` nuevo y pulsa **Commit changes**.

En uno o dos minutos la web ya tiene la lista nueva en todos los dispositivos.

## Probar en local

Abrir `index.html` con doble clic usa la copia de respaldo que va dentro del HTML. Para que lea `watchlist.csv` hace falta servirlo:

```
python -m http.server
```

y abrir http://localhost:8000.
