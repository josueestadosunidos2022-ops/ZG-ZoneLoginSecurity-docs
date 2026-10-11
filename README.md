# ZG ZoneLoginSecurity

## English

Pre-world account registration, encrypted login transport, sessions, administrator leases and audit controls for Minecraft 1.20.1 / Forge 47.4.x. Current pair: **server 1.1.3 + client 1.0.3**. Both files belong to one CurseForge project. The server requires ZoneCore 2.1.2+; ZoneLag 4.2.0+ is an optional server integration. ZoneSecurity 2.1.0 is **included inside the server JAR**; do not install a separate ZoneSecurity JAR. Use the ZoneLoginSecurity client, not the ZoneLag login client, when this authentication service owns accounts.

The login check runs before access to the world. The client pins the **public** GOCHOCASTLE server certificate fingerprint; it contains no private identity. Keep the matching server's persistent identity and account database private, backed up and unchanged during a routine JAR update. An explicit local fingerprint override takes precedence and a mismatch fails closed. Administrators grant time-limited OP only from the server console after login; no automatic OP on account login.

Config files live under `config/zoneloginsecurity/`, including `general.toml`, `registration.toml`, `credentials.toml`, `sessions.toml`, `administration.toml`, `storage.toml`, `audit.toml` and more. See [configuration and safe update guide](CONFIGURATION.md) and [release compatibility](RELEASES.md). Do not share account databases, identity files, passwords, invitation codes or production configuration.

## Español

Registro antes de entrar al mundo, transporte de login cifrado, sesiones, permisos OP temporales y auditoría para Minecraft 1.20.1 / Forge 47.4.x. Pareja: **servidor 1.1.3 + cliente 1.0.3** en un único proyecto CurseForge. El servidor requiere ZoneCore 2.1.2+; ZoneLag 4.2.0+ es una integración opcional. ZoneSecurity 2.1.0 viene **integrado en el JAR servidor**; no instales otro ZoneSecurity. Usa el cliente ZoneLoginSecurity cuando este sistema administra las cuentas, no el cliente de login ZoneLag.

El login se verifica antes de entrar al mundo. El cliente fija la huella **pública** del certificado de GOCHOCASTLE; no incluye identidad privada. Conserva y respalda en privado la identidad persistente y la base de cuentas del servidor al actualizar el JAR. Una huella local explícita tiene prioridad y una discrepancia deniega la conexión. El OP temporal se concede solo desde consola después del login; no se concede automáticamente al autenticarse.

Los TOML están en `config/zoneloginsecurity/`: `general.toml`, `registration.toml`, `credentials.toml`, `sessions.toml`, `administration.toml`, `storage.toml`, `audit.toml` y otros. Consulta [configuración y actualización segura](CONFIGURATION.md) y [compatibilidad](RELEASES.md). No compartas bases de cuentas, identidad privada, contraseñas, códigos ni TOML reales.

© Elgochogms. This repository contains documentation and a ZG avatar only; bundled third-party libraries retain their own licenses.

