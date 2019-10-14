# MathML

O HTML incorpora o padrão MathML. Trata-se de linguagem de marcação, baseada em XML, para represetanção de fórmulas matemáticas.  
Você pode ler mais sobre MathML em  (http://www.w3.org/Math)[http://www.w3.org/Math]. Para incorporar código MathML em seu documento HTML5, não preciso fazer declarações especiais. Basta escrever normalmente o código, iniciando com um elemento math.

```
    <math xmlns="http://www.w3.org/1998/Math/MathML">
        <mrow>
            <mi>x</mi>
            <mo>=</mo>
            <mfrac>
                <mrow>
                    <mo form="prefix">&minus;</mo>
                    <mi>b</mi>
                    <mo>&PlusMinus;</mo>
                    <msqrt>
                        <msup>
                            <mi>b</mi>
                            <mn>2</mn>
                        </msup>
                        <mo>&minus;</mo>
                        <mn>4</mn>
                        <mo>&InvisibleTimes;</mo>
                        <mi>a</mi>
                        <mo>&InvisibleTimes;</mo>
                        <mi>c</mi>
                    </msqrt>
                </mrow>
                <mrow>
                    <mn>2</mn>
                    <mo>&InvisbleTimes;</mo>
                    <mi>a</mi>
                </mrow>
            </mfrac>
        </mrow>
    </math>
```
