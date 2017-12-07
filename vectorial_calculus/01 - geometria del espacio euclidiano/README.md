# For Computer Graphic programmers

## Ejercicio 1
De lo visto en `sección 1.1 ejemplo 4`, dibujar un paralelogramo usando GLSL o HLSL.

## Ejercicio 2
Escribir la funcion mix de GLSL como la ecuacion parametrica de la linea que pasa por dos puntos. [ver en shadertoy](https://www.shadertoy.com/view/4lffRf)

  vec4 myMix(vec4 start, vec4 end, float mix)
  {
  	return start + (end - start) * mix;
  }

  void mainImage( out vec4 fragColor, in vec2 fragCoord )
  {
	  vec2 uv = fragCoord.xy / iResolution.xy;
    fragColor = myMix(vec4(1.0), vec4(0.0), 0.5 + 0.5*sin(iTime));
  }
