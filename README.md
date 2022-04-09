# Power simulations for the project: Canine Theory of Mind? Testing the concept of seeing and false-belief understanding in dogs.


| Study | Response variable                          | error structure | test condition                     | control condition                   | correlation | N  | power | design  | model                                                                                     |
|-------|--------------------------------------------|-----------------|------------------------------------|-------------------------------------|-------------|----|-------|---------|-------------------------------------------------------------------------------------------|
| 1     | mean choice correct (following the knower) | gaussian        | guesser absent / looking up / etc. | guesser present                     | 0.3         | 85 | 0.8   | within  | correlations                                                                              |
| 2     | first choice of unseen food bowl           | binomial        | sound-cue: 0.8                     | sound-control: 0.5                  |             | 76 | 0.81  | between | glm(resp~condition + sex +z.age, family=binomial)                                         |
| 3     | gaze congruent look                        | binomial        | transparent: 0.65                  | opaque: 0.4                         |             | 64 | 0.86  | within  | glmer(resp~condition + sex +z.age+z.trial+(1+condition+z.trial|subject), family=binomial) |
| 4     | follow the communicator's suggestion       | binomial        | false-belief: 0.65                 | true-belief: 0.3                    |             | 72 | 0.86  | between | glm(resp~condition + sex + first_baited_location +z.age, family=binomial)                 |
| 5     | wait response                              | binomial        | false-belief: 0.5                  | true-belief: 0.2                    |             | 32 | 0.88  | within  | glmer(resp~condition + sex +z.age+z.trial+(1+condition+z.trial|subject), family=binomial) |
| 6     | first look to true hiding location         | binomial        | false-belief: 0.3                  | true-belief: 0.65 / ignorance: 0.65 |             | 36 | 0.82  | within  | glmer(resp~condition + sex +z.age+z.session+(1+z.session|subject), family=binomial)       |                                                            |

## Structure 

```
.
├── Study 1           <-- Power analysis of correlation analysis.
├── Study 2           <-- Power analysis of first choice data using a Generalized Linear Model (GLM; binomial error structure).
├── Study 3           <-- Power analysis of gaze-congruent first looks using a Generalized Linear Mixed Model (GLMM; binomial error structure).
├── Study 4           <-- Power analysis of choices following the communicator's suggestion using a GLM (binomial error structure).
├── Study 5         <-- Power analysis of wait response using a GLMM (binomial error structure).
├── Study 6         <-- Power analysis of first look to true hiding position using a GLMM (binomial error structure).
```