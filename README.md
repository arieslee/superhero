修改自https://github.com/neversaysoso/superhero/

为th-message组件暴露更多的配置参数

使用方法

```bash
npm i nix-thor-x --save
```

1.配置main.js

```javascript
import thor from 'nix-thor-x'
import 'nix-thor-x/dist/index.css'
Vue.use(thor)
```

注：也可以不在main.js里引入，在具体页面按需引入相关组件

如：

```
import {ThMessage} from 'nix-thor-x';
import 'nix-thor-x/dist/index.css';
export default {
    name: "guestbookDialog",
    components: {
        ThMessage,
    },
    data(){
            return {
                messageData: [
                    {type:1,text:123123,isimg:false},
                    {type:2,text:123123,isimg:false},
                ],
                funclist: ["gallery","camera", "quick"],
                pulldownconfig:{}
            }
    }
}
```

## 聊天组件 th-message

```html
<th-message 
  ref="messgebox"
  :useText="true"
  :usePulldown="true"
  :pulldownConfig="pulldownconfig"
  :topPadding="120"
  :messageData="messageData" 
  :funcList="funclist" 
  :bigBtn="bigbtn"
  :textShow="false"
  :showInput="showinput"
  :selfFace="selfface" 
  :otherFace="otherface"
  :showEmoticon="true"
  @sendOut="senRequest"
  @galleryCall="gallery"
  @cameraCall="camera"
  @quickCall="quick"
  @bigBtnCall="btncall"
  @faceClick="faceclick"
  @msgClick="msgclick"
  @pulldownCall="pulldowncall">
</th-message>
```
