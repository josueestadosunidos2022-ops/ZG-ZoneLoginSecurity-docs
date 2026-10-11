# ZG ZoneLoginSecurity — releases and compatibility

Current protected pair: **server 1.1.3 + client 1.0.3** on one CurseForge project, Minecraft 1.20.1, Forge 47.4.x, Java 17. The server requires ZoneCore 2.1.2+ and optionally integrates ZoneLag 4.2.0+. ZoneSecurity is already integrated. The client contains the expected public GOCHOCASTLE certificate fingerprint; do not install it for a different server without an explicitly verified matching pin. Keep server identity, account DB and config private and backed up. Do not install test or unprotected JARs.

Validation: both clean Gradle builds; 74 server security checks and 5 client trust checks passed. The protected server started with protected Core 2.1.3 and Lag 4.3.1, listed `/zlogin` commands and stopped cleanly. No real player authentication, graphical client, full modpack or production hosting test was performed. Java obfuscation raises effort but cannot prevent all decompilation; security must rely on server-side controls and kept-private identity.

## Español

Pareja protegida: **servidor 1.1.3 + cliente 1.0.3** en un proyecto CurseForge para Minecraft 1.20.1, Forge 47.4.x y Java 17. El servidor requiere ZoneCore 2.1.2+ e integra ZoneLag 4.2.0+ opcionalmente. ZoneSecurity ya viene integrado. El cliente trae la huella pública esperada de GOCHOCASTLE; para otro servidor solo usa una huella explícita verificada. Conserva y respalda en privado identidad, base de cuentas y TOML. No instales JAR de pruebas ni sin protección.

Pasaron ambas compilaciones, 74 checks de seguridad y 5 de confianza cliente. El servidor protegido arrancó con Core 2.1.3 y Lag 4.3.1 protegidos, listó `/zlogin` y cerró limpio. Falta login real, cliente gráfico, modpack completo y hosting. La ofuscación no impide toda descompilación; la seguridad depende de controles de servidor e identidad privada.

