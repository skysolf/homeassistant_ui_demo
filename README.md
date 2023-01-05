# homeassistant 自定义UI 代码示例


```
type: picture-elements
image: /local/xxx/背景图
elements:
#徽章
  - type: state-badge
    entity: 设备实体ID号
    style:
      top: 9%
      left: 12%
  
#文字按钮
  - type: service-button
    title: 按钮文字
    style:
      top: 5%
      left: 45%
    service: 脚本ID
    service-data: null

 #一个灯状态图片
  - type: image
    entity: 设备实体ID号
    tap_action:
      action: none
    style:
      pointer-events: none
      top: 50%
      left: 50%
      width: 100%
      mix_blend_mode: lighten
    state_image:
      'off': /local/xxx/透明.png
      'on': /local/xxx/对应亮灯的图地址

#一个灯操作图标
  - type: state-icon
    entity: 同上的设备实体ID号
    tap_action:
      action: toggle
    #图标id
    icon: mdi:led-strip-variant
    state_color: true
    style:
      top: 77%
      left: 84%
 
  
