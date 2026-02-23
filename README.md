# camera\_avfoundation

Este é um fork do plugin [camera_avfoundation](https://pub.dev/packages/camera_avfoundation)

Ele adiciona o suporte a câmeras lógicas ([_builtInTripleCamera_, _builtInDualCamera_, _builtInDualWideCamera_](https://developer.apple.com/documentation/avfoundation/avcapturedevice/devicetype-swift.struct)) no iOS.

Esse projeto visa a alteração mínima do código original a fim de ficar fácil o remerge após uma eventual atualização da lib original. Assim, a camera principal irá ser substituída pela melhor câmera lógica disponível.

## Uso

No `pubspec.yaml`, adicione em `dependency_overrides`:

```
...
  camera: 0.11.3
...

dependency_overrides:
  camera_avfoundation:
    git:
      url: git@github.com:aleufms/camera_avfoundation.git
      ref: logical_cameras_support/x.y.z+a

```

onde `x.y.z+a` é a versão do plugin original
