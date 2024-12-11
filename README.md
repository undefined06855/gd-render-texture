# gd-render-texture

Custom render texture class for GD, with an easy to use interface

```cpp
// can be reused and stored
RenderTexture render(1920, 1080);

std::uniqure_ptr<uint8_t[]> data = render.captureData(scene /* format = RenderTexture::PixelFormat::RGBA */);

// IMPORTANT: image data is currently upside down, so you'll have to flip it yourself :P
//   this may change in a future version
```

## use as a sprite

```cpp
auto m_sprite = RenderTexture(1920, 1080).intoManagedSprite();
this->addChild(m_sprite.sprite);

// on update() {
m_sprite.render.capture(this);
// sprite node will now show the new capture

```