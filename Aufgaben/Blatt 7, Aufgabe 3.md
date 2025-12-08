**a)**
Ansatz: Gleicher Beweis wie Satz 5.13, (2)

Die Formel für Kovarianz ist $\mathbb{K}(X, Y)=\mathbb{E}[(X-\mathbb{E}X)(Y-\mathbb{E}Y)] = \mathbb{E}(XY) - \mathbb{E}X ~ \mathbb{E}Y$

Wir zeigen zuerst, dass die Verschiebungskonstanten ($a$ und $b$) wegfallen, danach die Skalierungsfaktoren ($\alpha$ und $\beta$)

Verschiebung:
ZZ: $\mathbb{K}(X + a, Y + b) = \mathbb{K}(X, Y)$

$$
\mathbb{K}(X+a, Y+b) = \mathbb{E}[(X+a-\mathbb{E}(X+a))(Y+b-\mathbb{E}(Y+b))]
$$
Mit 3-Uhr-Nachts-Regel:
$$
{} = \mathbb{E}[(X+a-\mathbb{E}(X)-a)(Y+b-\mathbb{E}(Y)-b]
$$
Weiter auflösen
$$
{} = \mathbb{E}[(X-\mathbb{E}X)(Y-\mathbb{E}Y)] = \mathbb{K}(X, Y)
$$
Verschiebung spielt also keine Rolle. Nun zu Skalierung
ZZ: $\mathbb{K}(\alpha X, \beta Y) = \alpha \beta \mathbb{K}(X, Y)$

$$
\mathbb{K}(\alpha X, \beta Y) = \mathbb{E}[(\alpha X - \mathbb{E}(\alpha X))(\beta Y - \mathbb{E}(\beta Y))]
$$
Laut Satz 5.5 (1) ist $\mathbb{E}$ linear, wir können also für $\mathbb{E}(\alpha X)$ auch $\alpha \mathbb{E}X$ schreiben
$$
{} = \mathbb{E}[(\alpha X-\alpha \mathbb{E}X)(\beta Y-\beta \mathbb{E}Y)]
$$
$\alpha$ und $\beta$ ausklammern
$$
{} = E[a * (X - \mathbb{E}X) * \beta * (Y-\mathbb{E}Y)]
$$
Wieder Linearität anwenden
$$
{} = \alpha\beta \mathbb{E}[(X-\mathbb{E}X)(Y-\mathbb{E}Y)] = \alpha\beta \mathbb{K}(X, Y)
$$
**b)**
Formel für Varianz nach Satz 5.13:
$$
\mathbb{V}X = \mathbb{E}(X - \mathbb{E}X)^2 = \mathbb{E}X^2 - (\mathbb{E}X)^2
$$
In diesem Fall
$$
\mathbb{V}(XY) = \mathbb{E}(XY)^2 - (\mathbb{E}(XY))^2 = \mathbb{E}(X^2 Y^2) - (\mathbb{E}(XY))^2
$$
Durch Unabhängigkeit der ZW können wir schreiben
$$
{} = \mathbb{E}(X^2) \mathbb{E}(Y^2) - (\mathbb{E}X)^2 (\mathbb{E}Y)^2
$$
NR:
$$
\mathbb{E}(X^2) = \mathbb{V}(X)+(\mathbb{E}X)^2
$$
in HR für $\mathbb{E}(X^2)$ und $\mathbb{E}(Y^2)$ einsetzen
$$
{} = (\mathbb{V}(X)+(\mathbb{E}X)^2)(\mathbb{V}(Y)+(\mathbb{E}X)^2)-(\mathbb{E}X)^2(\mathbb{E}Y)^2
$$
Ausmultiplizieren
$$
{} = \mathbb{V}(X)\mathbb{V}(Y) + \mathbb{V}(Y)(\mathbb{E}X)^2 + (\mathbb{E}X)^2\mathbb{V}(Y) + (\mathbb{E}X)^2 (\mathbb{E}Y)^2 - (\mathbb{E}X)^2 (\mathbb{E}Y)^2
$$
Die letzten beiden Terme heben sich auf, durch umsortieren erhalten wir die zu zeigende Formel
$$
{} = (\mathbb{E}X)^2 \mathbb{V}(Y) + (\mathbb{E}Y)^2 \mathbb{V}(X) + \mathbb{V}(X) \mathbb{V}(Y)
$$

**c)**
Wir verwenden für die Varianz wieder die originale Formel
$$
\mathbb{V}(X) = \mathbb{E}(X-\mathbb{E}X)^2
$$
Die Varianz misst die Abweichung zum Erwartungswert. Falls wir anstelle des Erwartungswertes eine andere Zahl einsetzen, kann die "Varianz" daraus nur größer oder gleich der echten Varianz sein. Heißt
$$
\mathbb{V}(X) = \min_{t \in \mathbb{R}} \mathbb{E}(X - t)^2
$$
und
$$
\mathbb{V(X)} \leq \mathbb{E}(X - t)^2
$$
Wähle $t = m := \frac{a + b}{2}$, also die Mitte des Intervalls (das wird auch noch für d wichtig).

Da $a \leq X \leq b$ gilt, gilt $|X - m| \leq \frac{b - a}{2}$ (jeder mögliche Wert von X kann nur max. das halbe Intervall von m entfernt sein).
Quadrieren
$$
(X - m)^2 \leq \left ( \frac{b-a}{2} \right )^2 = \frac{1}{4} (b-a)^2
$$

Der Erwartungswert ist darin eingeschlossen
$$
\mathbb{E}(X - m)^2 \leq \frac{1}{4} (b-a)^2
$$
Wir haben oben geschrieben, dass
$$
\mathbb{V(X)} \leq \mathbb{E}(X - t)^2
$$
Daraus folgt
$$
\mathbb{V}(X) \leq \frac{1}{4} (b-a)^2
$$
was zu zeigen war.

**d)**
Durch die gegebenen Wahrscheinlichkeiten gilt
$$
\mathbb{E}(X)=a * \frac{1}{2} + b * \frac{1}{2} = \frac{a+b}{2}
$$
Das ist genau der Mittelpunkt $m$
Damit
$$
\mathbb{V}(X) = \frac{1}{2} (a-m)^2 + \frac{1}{2}(b-m)^2
$$
NR:
$$
a-m = a - \frac {a+b} 2 = \frac {2a-a-b} 2 = \frac {a-b} 2 = -\frac{1}{2} (b-a)
$$
$$
b - m = b - \frac {a+b} 2 = \frac {2b - a - b} 2 = \frac{1}{2} (b-a)
$$
Quadrieren
$$
(a-m)^2 = \frac{(-1)^2}{2^2} (b-a)^2 = \frac{1}{4} (b-a)^2 = \frac {(b-a)^2} 4
$$
$$
(b-m)^2 = \frac{1^2}{2^2} (b-a)^2 = \frac{1}{4} (b-a)^2 = \frac {(b-a)^2} 4
$$
In Varianzformel einsetzen
$$
V(X) = \frac{1}{2} \frac {(b-a)^2} 4 + \frac{1}{2} \frac {(b-a)^2} 4 = \frac {(b-a)^2} 4 = \frac{1}{4} (b-a)^2
$$