# wanted_pre_onboarding
> Netlify ๋ฐฐํฌ </br>
[๐ DEMO SITE ๐](https://wanted-pre-onboarding-yeji.netlify.app/)

## ๊ตฌํํ ๋ฐฉ๋ฒ๊ณผ ์ด์ ์ ๋ํ ๊ฐ๋ตํ ๋ด์ฉ
> ๊ตฌํ๋๋ ์ปดํฌ๋ํธ๋ค์ด ๋ค๋ฅธ ์ฝ๋์์๋ ์ฌ์ฉ๋  ์ ์๋ค๋ผ๋ ์๊ฐ์ผ๋ก ์ฝ๋๋ฅผ ์์ฑํ์์ต๋๋ค. </br>
>
> 6๊ฐ์ ์ปดํฌ๋ํธ๋ฅผ ๊ฐ์ธ๋ Card ์ปดํฌ๋ํธ๋ props๋ก title๊ณผ children์ ์ด์ฉํ์ฌ ์ฌ์ฌ์ฉ์ฑ์ด ๊ฐ๋ฅํ๋๋ก ๋ง๋ค์์ต๋๋ค.</br>
>
> ์ปดํฌ๋ํธ๊ฐ ์ฆ๊ฐํจ์ ๋ฐ๋ผ ์คํ์ผ ์ฝ๋์ ์ผ๊ด์ฑ์ ์ ์งํ๊ณ  ์ถ์ด์ ์ฌ์ฉ๋๋ ์์์ styled-component์ ThemeProvider๋ฅผ ์ด์ฉํ์ฌ ์์ฑํ์์ต๋๋ค.

- **Toggle** 
๐`useState()`์ true false๊ฐ์ผ๋ก toggle์ on/off
- **Modal**
๐ `useState()`์ true false๊ฐ์ผ๋ก Modal ์ฐฝ ์ด๋ฆผ/ ๋ซํ
- **Tab**
๐ menu, content์ ๊ฐ์ ๋ณ๊ฒฝํ  ์ ์๋ ๊ฐ์ฒด ๋ณ์ ์์ฑ ๋ฐ ํด๋ฆญํ๋ menu๊ฐ์ ๋ฐ๋ผ content๋ด์ฉ ๋ณด์ผ ์ ์๊ฒ `useState()` ์ด์ฉํจ
- **Tag**
๐ ์๋ ฅ๋๋ Tag๊ฐ๊ณผ ์๋ ฅ๋์ด์ ธ ์๋ TagList๋ฅผ `useState()`๋ก ๋ง๋ค์ด์ ํ์ฉํจ
- **AutoComplete**
๐ ์๋ ฅ๋๋ value๊ฐ์ด๋ ์๋๊ฒ์๋ฆฌ์คํธ๋ฅผ `useState()`๋ก ๋ง๋ค์ด์ ํ์ฉํจ
- **ClickToEdit**
๐ name, age, ๋ณ๊ฒฝ๋ ๊ฐ editValue๋ฅผ `useState()`๋ก ๋ง๋ค์ด์ ํ์ฉํจ

## ๊ตฌํํ๋ฉด์ ์ด๋ ค์ ๋ ์ ๊ณผ ํด๊ฒฐ ๋ฐฉ๋ฒ (Error Handling Log)
| ๐คฏโ         | ์ด๋ ค์ ๋ ์  |
| ---------- | ------------- |
| ๐โ | <strong>ํด๊ฒฐ ๋ฐฉ๋ฒ</strong> |

- **Toggle**
> ๐คฏโ : toggle์ on / off ์ํ์ ๋ฐ๋ผ background๊ฐ ์ผ์ชฝ์์ ์ค๋ฅธ์ชฝ์ผ๋ก, ์ค๋ฅธ์ชฝ์์ ์ผ์ชฝ์ผ๋ก ์ด๋์ํค๋ ๋ฐฉ๋ฒ์ด ์ด๋ ค์ ์ต๋๋ค.</br>
> ๐โ : ์ฒ์์๋ transition๊ณผ animation์ ์ด์ฉํ์ฌ ์์ ๋ณ๊ฒฝ์ํค๋ ค๊ณ  ํ์์ผ๋ ๊ณ์๋ ์คํจ๋ฅผ ํตํด ๊ฒ์์ ํ์๊ณ , 
> ๊ทธ ๊ฒฐ๊ณผ `linear-gradient`์ `background-size`๋ฅผ ์ด์ฉํ์ฌ ๋ฐฉ๋ฒ์ ํด๊ฒฐํ์์ต๋๋ค.
```css
// ์ฌ๋ผ์ด๋ ์ ๋๋ฉ์ด์
background-color: ${props =>  props.theme.palette.gray};
background: linear-gradient(to left, ${props =>  props.theme.palette.gray} 50%, ${props =>  props.theme.palette.purple} 50%) right;
background-size: 200%;
transition: 0.5s ease-out;
```
- **Modal**
> ๐คฏโ: `Modal.js`์์ button๊ณผ Modal ์ฐฝ์ ๋ ๋ค ์ด๋ป๊ฒ ์ ๊ตฌํํ  ์ ์์๊น? ๋ผ๋ ์๊ฐ์ผ๋ก ์ฝ๋๋ฅผ ์์ฑํ๋ ๊ฒ ์ด๋ ค์ ์ต๋๋ค. </br>
> ๐โ : ์ฒ์์๋ `useState`์ `boolean`๊ฐ์ ํตํด ๋ฒํผ์ด ๋๋ฆฌ๋ฉด `modal`์ด ๋์ค๊ฒ ํ๊ธฐ๋ก ์ฝ๋๋ฅผ ์์ฑํ์์ง๋ง `if๋ฌธ`๊ณผ `else๋ฌธ`์ `button`์ด ๋ ๋ฒ ๋์์ 
> ๋ณ๋ก ์ข์ง ์์ ๋ฐฉ๋ฒ์ธ ๊ฒ ๊ฐ๋ค๋ ์๊ฐ์ ํ์์ต๋๋ค. ๊ทธ ๊ฒฐ๊ณผ `Modal์ฐฝ`๋ง ํจ์๋ก ๋นผ์!๋ผ๋ ์๊ฐ์ ํตํด  `ModalWindow()`๋ผ๋ ํจ์๋ฅผ ์์ฑํ์๊ณ , ๊ทธ ์์ ํ์คํธ๊ฐ ๋ฐ๋ ์ ์๋๋ก `props`๋ก `children`์ ์ด์ฉํ์ฌ ์์ฑํ์์ต๋๋ค. ๊ทธ ์ธ์ ํ์ํ ์ฐฝ์ด ๋ณด์ด๋ ์ง ์๋์ง ๋ํ๋ด๋ ๋ณ์ `visible`๊ณผ x๋ฒํผ์ ๋๋ฅด๋ฉด ์ฐฝ์ด ๊บผ์ง๋ ๋ณ์ `onCancel`๋ ํจ๊ป `props`๋ก ๋๊ฒจ์ฃผ์์ต๋๋ค.
```js
function ModalWindow({ visible, onCancel, children }){
    if (!visible) return null
    else
    return (
        <DarkBackground>
        <Mod.Modal>
            <Mod.Top>
                <span onClick={onCancel}>x</span>
            </Mod.Top>
            <Mod.Center>
                {children}
            </Mod.Center>
        </Mod.Modal>
        </DarkBackground>
    );
}
```
- **Tab**
> ๐คฏโ: ์ ํ๋ Tab์ด ๋๋ฌ์ก์ ๋ ์ ํ๋ ์์ ๋ฐ๊พธ๋ ๋ฐฉ๋ฒ์ด ์ด๋ ค์ ์ต๋๋ค. </br>
> ๐โ : ๋ณ๊ฒฝ๋ ์๋ง ๋ํ๋  ์ ์๊ฒ .active๋ฅผ className์ ์ง์ ํด์ฃผ์์ต๋๋ค. ์ ํ๋์ด์ง tab์ useState `isTabSelected`๋ณ์์ ๋ฃ์ด์ฃผ์๊ณ , mapํจ์์์ key๊ฐ๊ณผ `isTabSelected`๊ฐ์ด ๊ฐ์ผ๋ฉด .active๊ฐ ์๊ธฐ๋๋ก ๋ง๋ค์์ต๋๋ค. 
``` jsx
  className = {isTabSelected === idx ? "active" : ""}
```
```css
  &.active {
    color: ${props => props.theme.palette.white};
    box-shadow: inset 200px 0 0 0 ${props =>  props.theme.palette.purple };
}
```
- **Tag**
> ๐คฏโ: ์ ํํ ํ๊ทธ๋ ์ฝ๋๋ง ์ญ์ ํ๋ ๊ธฐ๋ฅ์ ์ฝ๋๋ฅผ ๊น๋ํ๊ฒ ์์ฑํ๋ ๋ฐฉ๋ฒ์ด ์ด๋ ค์ ์ต๋๋ค. </br> 
> ๐โ: ์ฒ์์๋ for๋ฌธ์ ํตํด isHashTagList์ ์๋ ๋ณ์์ index๊ฐ๊ณผ ์ญ์ ๋์ด์ง๋ index๊ฐ์ ๋น๊ตํ์ฌ ๊ฐ์ด ๊ฐ์ง ์๋ค๋ฉด isNewHashTagList์ ๊ฐ์ ๋ฃ๊ณ  ๊ทธ ํ์ `setIsHashTagList(isNewHashTagList)`๋ก ์์ฑํ์์ต๋๋ค. ํ์ง๋ง ์ฝ๋๋ฅผ ๋ ํธ๋ฆฌํ๊ฒ ์์ฑํ๋ ๋ฐฉ๋ฒ์ด ์๋๋ผ๋ ์๊ฐ์ผ๋ก ๋น์ทํ ํจ์๋ฅผ ์ฐพ๊ฒ ๋์๊ณ , `filterํจ์`๋ฅผ ์๊ฒ ๋์์ต๋๋ค.
๊ทธ ๊ฒฐ๊ณผ 7์ค์ด์๋ ์ฝ๋๊ฐ ๋จ 2์ค๋ก ๋ฐ๋ ์ ์์์ต๋๋ค.
```jsx
    const isNewHashTagList = []
    for(let i = 0; i < isHashTagList.length; i++){
      if(i !== id){
        isNewHashTagList.push(isHashTagList[i])
        setIsHashTagList(isNewHashTagList)
      }
    }
```
```jsx
    const isNewHashTagList = isHashTagList.filter((value, idx) => idx !== id);
    setIsHashTagList(isNewHashTagList);
```
- **AutoComplete**
> ๐คฏโ: input์ ๊ฐ์ด ๋ณ๊ฒฝ๋จ์ ๋ฐ๋ผ ์ผ์นํ๋ ๊ฒ์์ด๋ฅผ ๋ํ๋ด๋ ๋ฐฉ๋ฒ์ด ์ด๋ ค์ ์ต๋๋ค. </br> 
> ๐โ: ์ฒ์์๋ `onchangeValue`ํจ์์์ ์๋์์ฑ ๋ฆฌ์คํธ์ ๊ฒ์ํ ํค์๋๊ฐ ์๋ค๋ฉด ๊ฒ์๋ ๋ฆฌ์คํธ๊ฐ ๋์ฌ ์ ์๊ฒ ์ฝ๋๋ฅผ ์์ฑํ์์ต๋๋ค.
```jsx
    const onchangeValue = (e) => {
      setIsSerchedList(data.filter((item) => item.toLowerCase().includes(isInputValue.toLowerCase())));
      setIsInputValue(e.target.value);
    }
```
ํ์ง๋ง ๊ฒ์๋ ๋ฆฌ์คํธ์ ๋ฐ์์ด ๋๋ฆฌ๋ค๋ ๊ฒ์ ๊นจ๋ซ๊ณ  ๋ ํ `useEffect`ํจ์๋ฅผ ์ฌ์ฉํด์ ๊ฒ์์ ๋น๊ตํด์ฃผ์์ต๋๋ค. ๊ทธ ๊ฒฐ๊ณผ ์๋ง๊ฒ ๋์ํ๋ ๊ฒ์ ํ์ธ ํ  ์ ์์์ต๋๋ค.
```jsx
    const onchangeValue = (e) =>  setIsInputValue(e.target.value);
    useEffect(() => {
      if(isInputValue){
        setIsSerchedList(data.filter((item) => item.toLowerCase().includes(isInputValue.toLowerCase())))
      }
    // eslint-disable-next-line react-hooks/exhaustive-deps
    }, [isInputValue]);
```
- **ClickToEdit**
> ๐คฏโ: clickํ ๊ฒฐ๊ณผ ๊ฐ์ด ๋ฐ๋๊ฒ ๋ง๋๋ ๋ฐฉ๋ฒ์ด ์ด๋ ค์ ์ต๋๋ค. </br> 
> ๐โ: ์ฒ์์๋ `name`, `age`๋ก ์ํ๋ฅผ ๊ตฌํํ๋ ค๊ณ  ํ์์ต๋๋ค. ํ์ง๋ง ์๋ ฅ ๊ฐ ๋ณ๊ฒฝ ์ ๊ฒฐ๊ณผ๊ฐ์ด ๋ฐ๋ก ๋ฐ์๋์๊ณ , `editValue` ๋ณ์๋ฅผ ์๋กญ๊ฒ ๋ง๋ค๊ณ , input์ `onBlur` ํจ์๋ฅผ ์ด์ฉํ์ฌ ํฌ์ปค์ค๊ฐ ํด์ ๋  ๋  `editValue`๊ฐ์ด ๋ณ๊ฒฝ๋๋๋ก ๊ตฌํํ์์ต๋๋ค.
```jsx
function ClickToEdit() {

    const [name, setName] = useState('๊น์ฝ๋ฉ');
    const [age, setAge] = useState(20);
    const [editValue, setEditValue] = useState({name, age});

    const onBlurEdit = () => setEditValue({name, age})

  return (
    <>
    <Form.Item>
        <Form.Label>์ด๋ฆ</Form.Label>
        <Form.Input 
        value={name} 
        onChange={(e) => setName(e.target.value)}
        onBlur={onBlurEdit}
        />
    </Form.Item>
    <Form.Item>
        <Form.Label>๋์ด</Form.Label>
        <Form.Input 
        value={age} 
        onChange={(e) => setAge(e.target.value)}
        onBlur={onBlurEdit}
        />
    </Form.Item>
    <Content>
        <span>์ด๋ฆ {editValue.name}</span>
        <span>๋์ด {editValue.age}</span>
    </Content>
    </>
  );
}

export default ClickToEdit;
```

## ์์ธํ ์คํ ๋ฐฉ๋ฒ
* **Netlify ๋ฐฐํฌ**
[๐ DEMO SITE](https://wanted-pre-onboarding-yeji.netlify.app/) </br>
* **๋ก์ปฌ ํ๊ฒฝ**
1) `git clone https://github.com/Lee-ye-ji/wanted_pre_onboarding.git`
2) `cd custom-component`
3) `yarn i`
4) `yarn run start`
