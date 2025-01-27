# Exercise Set 1 for the Financial Markets Course

# The code is written in RStudio

---
output:
  html_document: default
  word_document: default
  pdf_document: default
---


Simon Tresor Ngabo - MATØK4 Gruppe 5.239

---
title: "Excercises 1"
author: "Financial Markets"
output:
  beamer_presentation:
    highlight: tango
  pdf_document:
    fig_caption: no
    keep_tex: yes
    highlight: tango
    number_section: yes
    toc: yes
  slidy_presentation:
    fig_caption: no
    highlight: tango
    theme: cerulean
  ioslides_presentation:
    highlight: tango
---

```{r, include = FALSE}
options(digits = 2)
## Remember to add all packages used in the code below!
missing_pkgs <- setdiff(c("mosaic"), rownames(installed.packages()))
if(length(missing_pkgs)>0) install.packages(missing_pkgs)
```

```{r, include=FALSE}
library(mosaic)
```

$\textbf{Question 1}$

i)
Irreflexive
X is weakly preferred to itself thus x ge x and x ge x, but strong preference implies that x ge x, but x is not ge x. Therefore an contradiction.

$$ x \succeq x,\quad \text{and}\quad x\nsucceq x $$

Transitive

$$X \succeq Y,\quad Y \nsucceq X,\quad Y \succeq Z, \quad Z \nsucceq Y$$

By transivity of $\succeq$

$$ X \succeq Z, \quad \text{and} \quad Z \nsucceq X $$

Thus 

$$ X \prec Z$$

ii)

Reflexive
By definition:

$$ X \succeq X, \quad \text{thus} \quad X \preceq X$$

Thus 

$$ X \sim X$$

Transitive

$$ X \succeq Y, \quad Y \succeq X,\quad Y \succeq Z,\quad Z \succeq Y $$

Thus by transitive of $\succeq$ :

$$ X \sim Z$$

Symmetric
We know that :

$$X \sim Y \quad \Rightarrow \quad X \succeq Y, \quad Y \succeq X, $$

$$X \succeq Y, \quad Y \succeq X \iff Y \succeq X, \quad X \succeq Y \Rightarrow Y \sim X$$

iii) 

The assumption :

$$ X \succ Y \succeq Z \Rightarrow X \succeq Y, \quad Y \nsucceq X \Rightarrow X \succeq Z$$

by transitivity.

$$ Z \preceq Y \npreceq X \quad \text{thus} \quad X \succ Z $$

$\textbf{Question 2}$

We know  that

$$X \succeq Y, \quad \Rightarrow \quad x_1>y_1 \quad \text{or} \quad x_1=y_1 \quad \text{and}  \quad x_2 \ge y_2.$$

and 

$$ Y \succeq Z, \quad \Rightarrow \quad y_1>z_1 \quad \text{or} \quad y_1=z_1 \quad \text{and}  \quad y_2 \ge z_2.$$

If we assume 

$$ X \succeq Y, \quad \text{and} \quad Y \succeq Z, $$

Which yields :

$$x_1>y_1 \quad \text{or} \quad x_1=y_1 \quad \text{and}  \quad x_2 \ge y_2, \quad \text{and} \quad y_1>z_1 \quad \text{or} \quad y_1=z_1 \quad \text{and}  \quad y_2 \ge z_2 $$

Thus there 4 cases, whom all should yield the same result 

1. case - assume

$$x_1 > y_1, \quad \text{and} \quad y_1 > z_1, \quad \text{then} \quad x_1 > z_1 \Rightarrow X \succeq Z   $$

2. case - assume

$$x_1 > y_1, \quad \text{and} \quad y_1=z_1, \quad y_2 \ge z_2,\quad \text{then} \quad x_1 > y_1 = z_1 \quad \Rightarrow  \quad X \succeq Z $$

3. case - assume

$$ x_1=y_1 \quad \text{and}  \quad x_2 \ge y_2, \quad \text{and } \quad y_1 > z_1, \quad \text{then} \quad x_1 = y_1 > z_1\quad \Rightarrow \quad X \succeq Z $$

4. case - assume

$$ x_1=y_1 \quad \text{and}  \quad x_2 \ge y_2, \quad \text{and } \quad \quad y_1=z_1 \quad \text{and}  \quad y_2 \ge z_2, \quad \text{then} \quad x_1 =y_1=z_1, \quad \text{and} \quad x_2 \ge y_2 \ge z_2 \quad \Rightarrow \quad X \succeq Z $$

ii)

$$\lim_{n\to\infty} (1-\frac{1}{n},1) = (1,1)$$

$$ \forall n, (1,0) \succeq (1-\frac{1}{n},1)$$

but 

$$ \lim_{n\to\infty}(1-\frac{1}{n},1) = (1,1) \succeq (1,0)$$

The sequence stays in the lower contour set, but the limit is not in the lower contour set. This implies that the lower contour set is not closed, therefore the preference relation is not continuous !

$\textbf{Risk Aversion}$

If u is increasing that means $u'(x)$ is a positive function, furthermore if u is DARA, 

$$-\frac{u''(x)}{u'(x)}$$

Is a decreasing function. Thus the denominator is positive, and the expression is negative, implying that $u''(x)$, must be a positive function, for u to be DARA.

If

$$-\frac{u''(x)}{u'(x)}$$

it implies 

$$\frac{u''(x)}{u'(x)}$$

is increasing. Therefore the derivative must be nonnegative i.e.

$$\frac{d}{dx}\left(-\frac{u''(x)}{u'(x)} \right) \ge 0$$

$$\frac{d}{dx}\left(-\frac{u''(x)}{u'(x)} \right) = \frac{u'''(x)u'(x)-(u''(x))^2}{(u'(x))^2}$$

Thus 

$$\frac{u'''(x)u'(x)-(u''(x))^2}{(u'(x))^2} \ge 0$$

Multiplying by $(u'(x))^2$ yields

$$u'''(x)u'(x)-(u''(x))^2 \ge 0$$

since $(u'(x))^2$ is a positive. This implies

$$u'''(x) \ge \frac{(u''(x))^2}{u'(x)} > 0$$

$\textbf{No insurance}$

1. no loss event occurs, thus the agent remains with wealth $w_0$
2. A loss event occurs, thus the agent wealths decrease to $w_0 - D$.

The lottery facing her is the list $L= (\pi, 1-\pi)$.


