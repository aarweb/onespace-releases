# OneSpace — instaladores

Aquí solo se publican los instaladores de OneSpace. Descárgalos desde
[Releases](https://github.com/aarweb/onespace-releases/releases/latest).

| Sistema | Estado |
|---|---|
| Linux x64 | Disponible (`.tar.gz`) |
| Windows x64 | Disponible (instalador `-setup.exe`) |
| macOS Apple Silicon | Disponible (`.dmg`) |

Los instaladores aún no llevan firma de Microsoft ni de Apple; la integridad se
garantiza con la firma OpenPGP de `SHA256SUMS`.

## Verificar la descarga

Cada release incluye `SHA256SUMS`, su firma `SHA256SUMS.asc` y la clave pública
`onespace-release-signing.pub.asc` (también en este repositorio).

Huella de la clave: `FC50 9615 2F0B 8505 CDF7  312A 38C6 A603 3FCF 75A4`

```sh
gpg --import onespace-release-signing.pub.asc
gpg --verify SHA256SUMS.asc SHA256SUMS
sha256sum -c SHA256SUMS
```

## Windows

Ejecuta `OneSpace-*-windows-x64-setup.exe`. SmartScreen avisará de un editor
desconocido: **Más información → Ejecutar de todas formas**.

Para verificar en PowerShell: `Get-FileHash .\OneSpace-*-setup.exe` y compara con `SHA256SUMS`.

## macOS

Abre el `.dmg` y arrastra OneSpace a Aplicaciones. La primera vez, **clic derecho
→ Abrir** (Gatekeeper bloquea apps sin notarizar). Solo Apple Silicon (M1 o posterior).

## Linux

```sh
tar -xzf OneSpace-*-linux-x64.tar.gz
./OneSpace-Beta/start-beta.sh
```

Requiere entorno gráfico y las bibliotecas de Electron (GTK3, NSS, ALSA y GBM).
