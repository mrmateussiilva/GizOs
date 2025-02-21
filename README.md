# GizOS - Kernel em Zig

GizOS é uma distribuição experimental de sistema operacional desenvolvida em Zig, com foco em simplicidade, desempenho e aprendizado sobre sistemas operacionais.

## 🌟 **Objetivos do Projeto**
- Criar um kernel simples e funcional em Zig.
- Explorar conceitos de gerenciamento de memória, interrupções e drivers.
- Servir como base para aprendizado e experimentação.

## 📁 **Estrutura do Projeto**
```
zig-kernel/
├── build.zig        # Script de build do Zig
├── linker.ld        # Arquivo de linkagem
├── src/
│   └── kernel.zig   # Código principal do kernel
├── boot/
│   └── limine.cfg   # Configuração do bootloader
└── iso/
    └── kernel.elf   # Arquivo ELF gerado
```

## 🚀 **Compilando e Executando**
1. **Instale as dependências:**
   - Zig (versão mais recente)
   - QEMU para emulação

2. **Compilar o kernel:**
```bash
zig build
```

3. **Criar a imagem ISO:**
```bash
mkdir -p iso/boot
cp zig-out/bin/kernel iso/boot/kernel.elf
cp boot/limine.cfg iso/limine.cfg
```

4. **Testar no QEMU:**
```bash
qemu-system-x86_64 -cdrom iso/kernel.elf
```

## 📜 **Funcionalidades Atuais**
- Exibição de mensagem no modo VGA
- Configuração básica do bootloader

## 🛠️ **Próximos Passos**
- [ ] Gerenciamento de interrupções (IDT e GDT)
- [ ] Gerenciamento de memória (Paging)
- [ ] Entrada de teclado
- [ ] Sistema de arquivos básico

## 🤝 **Contribuindo**
Este projeto está em desenvolvimento inicial. Sugestões, pull requests e feedback são bem-vindos!

## 📄 **Licença**
O GizOS é um projeto de código aberto licenciado sob a licença MIT.

