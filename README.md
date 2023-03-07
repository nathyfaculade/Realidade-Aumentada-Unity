## Olá, Devs!! 👋

<a href="http://www.colorado.edu/studentgroups/vrarclub/">
    <img src="https://github.com/jkredzvr/Unity-Vuforia-Tutorial/blob/master/Screenshots/VRLogo.png" alt="CU VRAR Club logo" title="CU VRAR Club logo" align="center" height="350" />
</a>

** Hoje vamos criar uma Realidade Aumentada no Unity com o Vulforia:**
<p>Essas duas ferramentas possibiltam a criar aplicações avançadas em AR de forma simples:</p>
<p>Para fazer o download do Unity, basta entrar no link abaixo: </p>
<p><a href= "https://unity.com/pt/download">Dowloand Unity<a/></p>

<p></p>
<p>Logo após você tem que fazer o download do Vulforia, que está dispónivel no link abaixo: </p>
<p> <a href="https://developer.vuforia.com/vui/auth/login?url=%2Fdownloads%2Fsdk%3F_%3D1678117884"> Download Vulforia</a></p>

<p></p>
<p>Logo após fazer o downloand dos dois aplicativos é necessário fazer uma conta para ter uma licença </p>
<p>Para poder criar a Target</p>
<p></p>
<img src="Target.png" align="center"/>

<p></p>

# Montando a imagem 
<p>Na imagem abaixo mostra a ultilização da imagem e como coloca a licença:</p>
<img src="License.png" align="center"/>
<p></p>

# Scripts Rotacionar o Cubo 

```javascrip
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Movimento : MonoBehaviour
{
    public Vector3 rotateAmount;
    void Start()
    {
        
    }

    // Update is called once per frame
    void Update()
    {
        transform.Rotate(rotateAmount * Time.deltaTime);
    }
}
```

# Movimento com o dado 
```javascrip
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Movimento : MonoBehaviour

{

    // Start is called before the first frame update

    Vector3 Vec;

    void Start()

    {    

    }

    // Update is called once per frame

    void Update()

    {

        Vec = transform.localPosition;

        Vec.y += Input.GetAxis("Jump") * Time.deltaTime * 5;

        Vec.x += Input.GetAxis("Horizontal") * Time.deltaTime * 5;

        Vec.z += Input.GetAxis("Vertical") * Time.deltaTime * 5;

        transform.localPosition = Vec;

    }

}


}
```
# Movimento com o teclado 

```javascrip
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Teclado : MonoBehaviour
{
    // Start is called before the first frame update
    void Start()
    {
        
    }

   // Update is called once per frame
    void Update()
    {
        if(Input.GetKey(KeyCode.LeftArrow))
        {
            transform.Translate(0.1f, 0f, 0f );
        }
        if(Input.GetKey(KeyCode.RightArrow))
        {
            transform.Translate(-0.1f, 0f, 0f );
        }
        if(Input.GetKey(KeyCode.DownArrow))
        {
            transform.Translate(0f, 0f, 0.1f );
        }
        if(Input.GetKey(KeyCode.UpArrow))
        {
            transform.Translate(0.1f, 0f, -0.1f );
        }

    }
}
```


# Rotacionar a imagem
**Para fazer a rotação do cubo é preciso colocar o eixo de rotação**
<p>X = 50, Y = 50, Z = 50.</p>
<img src="rotacao.png" align="center"/>
