# Paquetes de Firmware y Adaptación de Dispositivos (CosmicOS)

## Alcance (Secciones 3, 10.6, 10.7 y 16.4 de CosmicOS Spec v0.2.5)

- **Aislamiento de hardware:**
  - El módem celular opera con firmware propietario aislado obligatoriamente mediante IOMMU / VFIO con DMA restringido.
  - El chip Bluetooth se gestiona detrás de `cbrokerd` con BlueZ en dominio SELinux dedicado.
- **Audio y Llamadas:**
  - Perfiles de enrutado ALSA UCM específicos por placa y modelo para alternar correctamente entre micrófono, auricular y altavoz con PipeWire y ModemManager.
- **Árboles de Dispositivos (Device Trees):**
  - Soporte para plataformas ARM64 de referencia (Qualcomm Snapdragon / Google Tensor) y RISC-V.
