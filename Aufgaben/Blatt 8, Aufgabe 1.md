Tschebyschev-Ungleichung ist definiert durch:

$$
\mathbb{P}(|X - \mathbb{E}X| \geq \epsilon) \leq \frac{\mathbb{V}X}{\epsilon^2}
$$
Wir haben Abweichungstoleranz $\epsilon = 3\% = 0.03$ und Sicherheit $95\%$ (heißt Fehlerwahrscheinlichkeit $5\%$). Es muss also $\mathbb{P}(|\overline X -X| \geq 0.03) \leq 0.05$ gelten ($\overline X$ ist unsere Stichprobe, $X$ das finale Resultat der Wahl).

Da wir einen amtierenden Präsidenten und einen Herausforderer haben, ist die Wahlentscheidung ein Bernoulli-Experiment (Kandidat 1 wird mit Wkeit $p$ gewählt, Kandidat 2 mit $(1-p)$).

Die Varianz der Stichprobe (mit Größe $n$) ist

$$
\mathbb{V}(\overline X) = \frac{p \cdot (1-p)}{n}
$$

$p$ kennen wir nicht (das ist ja genau das was wir ausrechnen wollen), Annahme vom Worst Case: $p = \frac{1}{2}$, dann ist $p*(1-p) = \frac{1}{2} \cdot \frac{1}{2} = \frac{1}{4}$. Also gilt für die Varianz

$$
\mathbb{V}(\overline X) \leq \frac{1}{4n}
$$
Das können wir in die Tschebyschev-Ungleichung einsetzen

$$
\mathbb{P}(|\overline X - X| \geq 0.03) \leq \frac{\mathbb{V}(\overline X)}{\epsilon^2} \leq \frac{1}{4n \epsilon^2} \leq 0.05
$$
Gleichung auflösen

$$
\frac{1}{4n\epsilon^2} \leq 0.05 \stackrel{\cdot 4n\epsilon^2}{\leftrightarrow}
1\leq 0.05 \cdot 4n\epsilon^2 \leftrightarrow
1 \leq 0.2n\epsilon^2 \stackrel{\div 0.2\epsilon^2}\leftrightarrow
n \geq \frac{1}{0.2\epsilon^2} \leftrightarrow
n \geq \frac{5}{\epsilon^2}
$$
$\epsilon = 0.03$ einsetzen

$$
n \geq \frac{5}{0.03^2} = \frac{5}{0.0009} = 5555.5555\dots
$$
Es müssen also laut Tschebyschev-Ungleichung mindestens 5556 Personen befragt werden, um die gewünschte Sicherheit und Abweichung mit der Stichprobe zu erhalten.