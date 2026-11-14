# wuwa-x-es-db

Base de datos publica de los tweets de [@WW_ES_Official](https://x.com/WW_ES_Official) (Wuthering Waves ES).

- `wuwa_es.js` se genera automaticamente desde [wuwa-x-es-archive](https://github.com/k4wai1/wuwa-x-es-archive).
- No editar a mano.
- **Nunca se borran tweets**: solo se anaden.

## Uso

```html
<script src="https://cdn.jsdelivr.net/gh/k4wai1/wuwa-x-es-db@main/wuwa_es.js"></script>
<script>
  console.log(WUWA_ES.meta.count);  // numero de tweets
  console.log(WUWA_ES.tweets[0]);   // el mas antiguo
</script>
```

## Estructura

```js
window.WUWA_ES = {
  meta: { updated_at, count, first, last, source, generated_by },
  tweets: [{ id, date, text, type, url, media: [{ kind, url }] }]
}
```

Los `id` son strings: los IDs de X superan 2^53.

Generado por [wuwa-x-es-archive](https://github.com/k4wai1/wuwa-x-es-archive).
