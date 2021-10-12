# emotion-JSS

this is a great package for JSS and Provides you with much more productivity.

I'm using `@emotion/styled`;

`$. npm i @emotion/styled`

use case example:

```js
import styled from '@emotion/styled';

interface WrapperProps {
  color: string;
}

const Wrapper = styled('div')<WrapperProps>`
  background-color: red;
  color: ${(props) => props.color};
  padding: 1rem;
  &:hover {
    background-color: ${(props) => props.color};
  }
`

const TestComponent = () => {
  const [color, setColor] = useState('white');
  
  const handleChange = (e: React.ChangeEvent<HTMLInputElement>) => setColor(e.target.value);
  
  const resetColor = setColor('');
  
  return (
    <>
     <input value={color} onChange={handleChange} />
     <Wrapper color={color}>
       <h1>Heading</h1>
       <button onClick={resetColor}>button</button>
     </Wrapper>
    </>
  )
}
```
