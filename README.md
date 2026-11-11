# OneSpace — instaladores

Aquí solo se publican los instaladores de OneSpace. Descárgalos desde
[Releases](https://github.com/aarweb/onespace-releases/releases/latest).

| Sistema | Estado |
|---|---|
| Linux x64 | Disponible (`.tar.gz`) |
| Windows | Próximamente |
| macOS | Próximamente |

## Verificar la descarga

Cada release incluye `SHA256SUMS`, su firma `SHA256SUMS.asc` y la clave pública
`onespace-release-signing.pub.asc` (también en este repositorio).

Huella de la clave: `FC50 9615 2F0B 8505 CDF7  312A 38C6 A603 3FCF 75A4`

```sh
gpg --import onespace-release-signing.pub.asc
gpg --verify SHA256SUMS.asc SHA256SUMS
sha256sum -c SHA256SUMS
```

## Linux

```sh
tar -xzf OneSpace-*-linux-x64.tar.gz
./OneSpace-Beta/start-beta.sh
```

Requiere entorno gráfico y las bibliotecas de Electron (GTK3, NSS, ALSA y GBM).
