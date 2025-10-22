# 🐧 Basic Commands for Linux

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Linux](https://img.shields.io/badge/OS-Linux-blue.svg)](https://www.linux.org/)
[![Bash](https://img.shields.io/badge/Shell-Bash-green.svg)](https://www.gnu.org/software/bash/)
[![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](CONTRIBUTING.md)

> *"The command line is the ultimate seat of power on any Unix system."* - Brian W. Kernighan

Una colección completa y práctica de comandos esenciales de Linux para usuarios de todos los niveles, desde principiantes hasta administradores de sistemas experimentados.

## 📋 Tabla de Contenidos

- [🎯 Descripción](#-descripción)
- [🔧 Estructura del Repositorio](#-estructura-del-repositorio)
- [🚀 Inicio Rápido](#-inicio-rápido)
- [📚 Módulos de Aprendizaje](#-módulos-de-aprendizaje)
- [💡 Casos de Uso](#-casos-de-uso)
- [🤝 Contribuciones](#-contribuciones)
- [📄 Licencia](#-licencia)
- [🔗 Enlaces Útiles](#-enlaces-útiles)

## 🎯 Descripción

Este repositorio contiene una guía completa de comandos de Linux organizados por categorías y niveles de dificultad. Perfecto para:

- **Pentesting y Ethical Hacking** 🕵️‍♂️
- **Administración de Sistemas** ⚙️
- **DevOps y Automatización** 🤖
- **Análisis Forense Digital** 🔍
- **Desarrollo y Scripting** 💻

## 🔧 Estructura del Repositorio

```
Basic-Commands-for-Linux/
├── commands linux 1/
│   └── README.md                    # Comandos básicos fundamentales
├── commands linux 2 (ficheros)/
│   └── comandos_linux.md           # Gestión avanzada de archivos
├── commands linux 3/
│   └── [Próximamente]              # Comandos de red y seguridad
├── scripts/
│   └── [Próximamente]              # Scripts de automatización
└── cheatsheets/
    └── [Próximamente]              # Hojas de referencia rápida
```

## 🚀 Inicio Rápido

### Clonar el Repositorio
```bash
git clone https://github.com/tu-usuario/Basic-Commands-for-Linux.git
cd Basic-Commands-for-Linux
```

### Navegación Rápida
```bash
# Comandos básicos
cat "commands linux 1/README.md"

# Gestión de archivos
cat "commands linux 2 (ficheros)/comandos_linux.md"
```

## 📚 Módulos de Aprendizaje

### 🟢 Nivel Principiante
**📁 commands linux 1/**
- Navegación básica del sistema
- Gestión fundamental de archivos
- Comandos de información del sistema
- Primeros pasos en la terminal

### 🟡 Nivel Intermedio
**📁 commands linux 2 (ficheros)/**
- Operaciones avanzadas con archivos
- Permisos y propiedades
- Búsqueda y filtrado
- Manipulación de texto

### 🔴 Nivel Avanzado
**📁 commands linux 3/** *(En desarrollo)*
- Comandos de red y conectividad
- Monitoreo y análisis del sistema
- Seguridad y auditoría
- Automatización y scripting

## 💡 Casos de Uso

### Para Ethical Hackers
```bash
# Reconocimiento de sistema
uname -a && whoami && id
cat /etc/passwd | grep -E '/bin/(bash|sh)'
netstat -tuln | grep LISTEN
```

### Para SysAdmins
```bash
# Monitoreo rápido del sistema
df -h && free -h && uptime
ps aux --sort=-%cpu | head -10
journalctl -f --since "1 hour ago"
```

### Para Desarrolladores
```bash
# Búsqueda en código
find . -name "*.py" -exec grep -l "function_name" {} \;
grep -r "TODO" --include="*.js" .
```

## 🔥 Comandos Destacados

### One-Liners Poderosos
```bash
# Encontrar archivos grandes
find / -type f -size +100M 2>/dev/null | head -10

# Monitoreo de procesos en tiempo real
watch -n 1 'ps aux --sort=-%cpu | head -20'

# Backup rápido con timestamp
tar -czf backup_$(date +%Y%m%d_%H%M%S).tar.gz /ruta/importante
```

### Comandos de Seguridad
```bash
# Verificar conexiones activas
ss -tuln | grep :22

# Análisis de logs de autenticación
sudo grep "Failed password" /var/log/auth.log | tail -20

# Verificar integridad de archivos
find /etc -type f -exec sha256sum {} \; > system_baseline.txt
```

## 🛡️ Consideraciones de Seguridad

⚠️ **IMPORTANTE**: Estos comandos son para fines educativos y administración legítima de sistemas. Úsalos responsablemente:

- Siempre en sistemas propios o con autorización explícita
- Respeta las políticas de seguridad de tu organización
- Considera el impacto de comandos destructivos
- Mantén backups antes de modificaciones importantes

## 🤝 Contribuciones

¡Las contribuciones son bienvenidas! Por favor:

1. Fork el repositorio
2. Crea una rama para tu feature (`git checkout -b feature/nuevo-comando`)
3. Commit tus cambios (`git commit -m 'Agregar nuevo comando'`)
4. Push a la rama (`git push origin feature/nuevo-comando`)
5. Abre un Pull Request

### Formato de Contribuciones
- Incluye ejemplos prácticos
- Añade explicaciones claras
- Considera diferentes distribuciones
- Prueba los comandos antes de enviar

## 📊 Estadísticas del Proyecto

- **Comandos Documentados**: 150+
- **Categorías**: 8
- **Ejemplos Prácticos**: 200+
- **Scripts de Automatización**: En desarrollo

## 🎯 Roadmap

- [ ] Comandos de red y conectividad
- [ ] Scripts de automatización
- [ ] Cheatsheets en PDF
- [ ] Ejemplos de pentesting ético
- [ ] Integración con Docker
- [ ] Guías de troubleshooting

## 📄 Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para más detalles.

## 🔗 Enlaces Útiles

### Documentación Oficial
- [Linux Man Pages](https://man7.org/linux/man-pages/)
- [GNU Coreutils](https://www.gnu.org/software/coreutils/)
- [Bash Manual](https://www.gnu.org/software/bash/manual/)

### Recursos de Aprendizaje
- [ExplainShell](https://explainshell.com/) - Explica comandos de shell
- [TLDR Pages](https://tldr.sh/) - Ejemplos simplificados
- [Linux Journey](https://linuxjourney.com/) - Tutoriales interactivos

### Herramientas de Pentesting
- [Kali Linux Tools](https://www.kali.org/tools/)
- [OWASP Testing Guide](https://owasp.org/www-project-web-security-testing-guide/)
- [SecLists](https://github.com/danielmiessler/SecLists)

## 👥 Autores

- **4peir0n** - *Creador y Mantenedor Principal* - [@4peir0n](https://github.com/4peir0n)

## 🙏 Agradecimientos

- Comunidad de Linux y Open Source
- Contribuidores del proyecto
- Mantenedores de herramientas GNU/Linux

---

<div align="center">

**⭐ Si este repositorio te fue útil, no olvides darle una estrella ⭐**

Made with 💻 and ☕ for the Linux community

[🐛 Reportar Bug](https://github.com/tu-usuario/Basic-Commands-for-Linux/issues) •
[💡 Solicitar Feature](https://github.com/tu-usuario/Basic-Commands-for-Linux/issues) •
[📖 Documentación](https://github.com/tu-usuario/Basic-Commands-for-Linux/wiki)

</div>
