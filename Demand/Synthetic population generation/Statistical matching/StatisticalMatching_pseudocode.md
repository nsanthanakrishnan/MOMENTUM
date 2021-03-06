# Statistical matching

Inputs:

  * Household weights computed from PopGen: w<sub>h</sub>

  * List with the generated synthetic population and their attributes

  * Sample from household travel surveys

<p> 1. Define matching attributes in the synthetic population:
 <pre>
  <b>for each</b> observation n in the synthetic population <b>do</b>
    create a list of matching attributes and their values 
     &alpha;<sub>n </sub> = (&alpha;<sub>n,1</sub>, ... ,&alpha;<sub>n,1</sub>)
  <b>end for</b>
 </pre>
<p> 2. Define matching attributes in the survey sample:
<pre>
  <b>for each</b>  observation s in the sample <b>do</b>
    create a list with the respective matching attributes and their values
     &alpha;<sub>s </sub> = (&alpha;<sub>s,1</sub>, ... ,&alpha;<sub>s,1</sub>)
  <b>end for</b>
</pre>
<p> 3. For each observation n of the synthetic population match the predefined attributes in the sample:
<pre>
  <b>for each</b> observation s in the household travel survey sample <b>do</b>
    define set of observations H_n^*  in sample that match k attributes to the synthetic population: 
     H<sub>n*</sub> = {s|&alpha;<sub>(s,1:k)</sub>=&alpha;<sub>(n,1:k)</sub>} 
  <b>end for</b>
</pre>
<p> 4. Sample a household s from the set H_n^*   using a probability distribution
<pre>
 <b>for each</b>  observation n in the synthetic population <b>do</b>

   ![image1](https://user-images.githubusercontent.com/79461107/116729200-2f3d0600-a9e7-11eb-89b6-a335e1a90025.PNG)
 <b>end for</b>
</pre>



