# Orbital Elements Calculation
This README contains detailed step-by-step solutions for Problems 4.3–4.7: computing the **classical orbital elements** 
(
𝑎
,
𝑒
,
𝑖
,
Ω
,
𝜔
,
𝜃
)
from given position vector 
𝑟
and velocity vector 
𝑣
in the geocentric equatorial frame.
We use Earth's gravitational parameter:

$$\mu = 398600 \; km^3/s^2$$

---

## General Formulas

- Position and velocity magnitudes:

$$r = ||\vec{r}||, \quad v = ||\vec{v}||$$

- Specific angular momentum:

$$\vec{h} = \vec{r} \times \vec{v}, \quad h = ||\vec{h}||$$

- Node vector:

$$\vec{n} = \vec{k} \times \vec{h}, \quad n = ||\vec{n}||, \; \vec{k} = (0,0,1)$$

- Eccentricity vector:

$$\vec{e} = \frac{\vec{v} \times \vec{h}}{\mu} - \frac{\vec{r}}{r}, \quad e = ||\vec{e}||$$

- Inclination:

$$i = \cos^{-1}\left(\frac{h_z}{h}\right)$$

- RAAN:

$$
\Omega =
\begin{cases}
\cos^{-1}\left(\frac{n_x}{n}\right), & n_y \geq 0 \\
360^\circ - \cos^{-1}\left(\frac{n_x}{n}\right), & n_y < 0
\end{cases}
$$

- Argument of perigee:

$$
\omega = \cos^{-1}\left(\frac{\vec{n}\cdot\vec{e}}{ne}\right), \quad
\text{if } e_z < 0 \; \Rightarrow \; \omega = 360^\circ - \omega
$$

- True anomaly:

$$
\theta = \cos^{-1}\left(\frac{\vec{e}\cdot\vec{r}}{er}\right), \quad
\text{if } \vec{r}\cdot\vec{v} < 0 \; \Rightarrow \; \theta = 360^\circ - \theta
$$

- Specific orbital energy:

$$\epsilon = \frac{v^2}{2} - \frac{\mu}{r}$$

- Semi-major axis:

$$a = -\frac{\mu}{2\epsilon}$$

- Semi-latus rectum:

$$p = \frac{h^2}{\mu}$$

---

# Problem 4.3 — Detailed Solution

Given:

$\mathbf r = \langle 2615,\ 15881,\ 3980\rangle\ \mathrm{km},\qquad \mathbf v = \langle -2.767,\ -0.7905,\ 4.980\rangle\ \mathrm{km/s}.$

**Step 1 — magnitudes**

$r = 16579.6498\ \mathrm{km},\qquad v = 5.751659\ \mathrm{km/s}.$

**Step 2 — angular momentum**

$\mathbf h = \mathbf r\times\mathbf v = \langle 82233.57,\ -24035.36,\ 41875.5695\rangle\ \mathrm{km^2/s}.$

$h = 95\,360.484\ \mathrm{km^2/s}.$

**Step 3 — eccentricity vector**

$\mathbf e = \frac{\mathbf v\times\mathbf h}{\mu} - \frac{\mathbf r}{r} = \langle 0.0595205,\ 0.360235,\ 0.0898801\rangle.$

$e = 0.3760187.$

**Step 4 — inclination**

$i = \cos^{-1}\!\left(\frac{h_z}{h}\right) = 63.9517^\circ.$

**Step 5 — node vector and RAAN**

$\mathbf n = \mathbf k\times\mathbf h = \langle 24035.36,\ 82233.57,\ 0\rangle,\qquad n = 85674.142.$

Since $n_y>0$:

$\Omega = \cos^{-1}\!\left(\frac{n_x}{n}\right) = 73.7073^\circ.$

**Step 6 — argument of perigee**

$\omega = \cos^{-1}\!\left(\frac{\mathbf n\cdot\mathbf e}{ne}\right) = 15.4297^\circ.$

(Here $e_z>0$ so no quadrant correction needed.)

**Step 7 — true anomaly**

$\theta = \cos^{-1}\!\left(\frac{\mathbf e\cdot\mathbf r}{er}\right) = 0.06764^\circ.$

(And $\mathbf r\cdot\mathbf v>0$ so we keep this value.)

**Step 8 — energy, semi-major axis, parameter**

$\varepsilon = \frac{v^2}{2}-\frac{\mu}{r},\qquad a = -\frac{\mu}{2\varepsilon} = 26\,570.742\ \mathrm{km}.$

$p = \frac{h^2}{\mu} = 22\,813.903\ \mathrm{km}.$

**Result (4.3):**

$e=0.3760,\quad h=95\,360\ \mathrm{km^2/s},\quad i=63.95^\circ,\quad \Omega=73.71^\circ,\quad \omega=15.43^\circ,\quad \theta=0.06764^\circ.$

---

# Problem 4.4 — Detailed Solution

Given:

$\mathbf r = \langle 0,\ 0,\ 12670\rangle\ \mathrm{km},\qquad \mathbf v = \langle -3.874,\ 0,\ -0.7905\rangle\ \mathrm{km/s}.$

**Step 1 — magnitudes**

$r = 12670\ \mathrm{km},\qquad v = 3.953829\ \mathrm{km/s}.$

**Step 2 — angular momentum**

$\mathbf h = \langle 0,\ -49083.58,\ 0\rangle\ \mathrm{km^2/s},\qquad h = 49\,083.58\ \mathrm{km^2/s}.$

**Step 3 — eccentricity vector**

$\mathbf e = \langle -0.0973421,\ 0,\ -0.522956\rangle,\qquad e = 0.531938.$

**Step 4 — inclination**

$i = \cos^{-1}\!(0) = 90^\circ\quad\text{(polar orbit)}.$

**Step 5 — node vector and RAAN**

$\mathbf n = \langle 49083.58,\ 0,\ 0\rangle \Rightarrow \Omega = 0^\circ.$

**Step 6 — argument of perigee**

$\omega = \cos^{-1}\!\left(\frac{\mathbf n\cdot\mathbf e}{ne}\right) = 259.456^\circ.$

(Here $e_z<0$ — quadrant correction applied.)

**Step 7 — true anomaly**

$\theta = \cos^{-1}\!\left(\frac{\mathbf e\cdot\mathbf r}{er}\right) = 190.544^\circ.$

($\mathbf r\cdot\mathbf v<0$ so we use the supplementary quadrant.)

**Step 8 — semi-major axis**

$a = 8429.286\ \mathrm{km}.$

**Result (4.4):**

$h\approx 49\,080\ \mathrm{km^2/s},\quad e=0.5319,\quad i=90^\circ,\quad \Omega=0^\circ,\quad \omega=259.46^\circ,\quad \theta=190.54^\circ.$

> *Note:* some solution sets list $\Omega=90^\circ$ with a compensating shift in $\omega$; the physically invariant quantity is the argument of latitude $u=\omega+\theta$, here placing $\mathbf r$ on +$\mathbf k$.

---

# Problem 4.5 — Detailed Solution

Given:

$\mathbf r = \langle 6472.7,\ -7470.8,\ -2469.8\rangle\ \mathrm{km},\qquad \mathbf v = \langle 3.9914,\ 2.7916,\ -3.2948\rangle\ \mathrm{km/s}. $

**Step 1 — magnitudes**

$r = 10188.651\ \mathrm{km},\qquad v = 5.880477\ \mathrm{km/s}.$

**Step 2 — angular momentum**

$\mathbf h = \langle 31509.486,\ 11468.292,\ 47888.140\rangle,\qquad h = 58\,460.614\ \mathrm{km^2/s}.$

**Step 3 — eccentricity vector**

$\mathbf e = \langle -0.205104,\ -0.006738,\ 0.136568\rangle,\qquad e = 0.246503.$

**Step 4 — inclination**

$i = \cos^{-1}\!\left(\frac{h_z}{h}\right) = 34.99998^\circ \approx 35^\circ.$

**Step 5 — node vector and RAAN**

$\mathbf n = \langle -11468.292,\ 31509.486,\ 0\rangle \Rightarrow \Omega = 110.000^\circ.$

**Step 6 — argument of perigee**

$\omega = \cos^{-1}\!\left(\frac{\mathbf n\cdot\mathbf e}{ne}\right) = 74.996^\circ.$

($e_z>0$ so no sign correction needed.)

**Step 7 — true anomaly**

$\theta = \cos^{-1}\!\left(\frac{\mathbf e\cdot\mathbf r}{er}\right) = 130.004^\circ.$

(Here $\mathbf r\cdot\mathbf v<0$ so the quadrant yields the stated value.)

**Step 8 — semi-major axis**

$a = 9128.821\ \mathrm{km}.$

**Result (4.5):**

$h\approx 58\,461\ \mathrm{km^2/s},\quad e=0.2465,\quad i=35^\circ,\quad \Omega=110^\circ,\quad \omega=75^\circ,\quad \theta=130^\circ.$

---

# Problem 4.6 — True Anomaly ($\theta$)

Given:

$\mathbf r = \langle -6634.2,\ -1261.8,\ -5230.9\rangle,\quad \mathbf v = \langle 5.7644,\ -7.2005,\ -1.8106\rangle,\quad \mathbf e = \langle -0.40907,\ -0.48751,\ -0.63640\rangle.$

Compute:

$e = 0.90020,\quad r = 8542.076\ \mathrm{km}.$

Dot product:

$\mathbf e\cdot\mathbf r = 7664.52 \Rightarrow \cos\theta = \frac{\mathbf e\cdot\mathbf r}{er} = 0.86602.$

So $\theta = 30.00^\circ$ or $330.00^\circ$. Use radial velocity sign:

$\mathbf r\cdot\mathbf v = -12532.6 < 0 \Rightarrow \dot r < 0\;\text{(flying toward perigee)}.$

This implies $\sin\theta<0$ so the correct true anomaly is

$\theta = 330.00^\circ.$

**Result (4.6):** $\theta\approx 330^\circ.$

---

# Problem 4.7 — Inclination ($i$)

Given:

$\mathbf r = \langle -6634.2,\ -1261.8,\ -5230.9\rangle,\quad \mathbf e = \langle -0.40907,\ -0.48751,\ -0.63640\rangle.$

Both $\mathbf r$ and $\mathbf e$ lie in the orbital plane. A normal to the plane is

$\mathbf h_{\rm dir} \propto \mathbf r\times\mathbf e.$

Compute:

$\mathbf h_{\rm dir} = \mathbf r\times\mathbf e = \langle -1747.11,\ -2082.20,\ 2718.07\rangle.$

$i = \cos^{-1}\!\left(\frac{(\mathbf h_{\rm dir})_z}{\|\mathbf h_{\rm dir}\|}\right) = \cos^{-1}(0.707106) \approx 45.0^\circ.$

**Result (4.7):** $i = 45^\circ.$

---

# Final Answers Summary

* **4.3:** $e=0.3760,\ h=95\,360\ \mathrm{km^2/s},\ i=63.95^\circ,\ \Omega=73.71^\circ,\ \omega=15.43^\circ,\ \theta=0.06764^\circ.$
* **4.4:** $e=0.5319,\ h\approx49\,080,\ i=90^\circ,\ \Omega=0^\circ,\ \omega=259.46^\circ,\ \theta=190.54^\circ.$
* **4.5:** $e=0.2465,\ h\approx58\,461,\ i=35^\circ,\ \Omega=110^\circ,\ \omega=75^\circ,\ \theta=130^\circ.$
* **4.6:** $\theta\approx330^\circ.$
* **4.7:** $i=45^\circ.$

---

## Python reproduction (example snippet)

```python
import numpy as np

mu = 398600.0  # km^3/s^2

def orbital_elements(r_vec, v_vec):
    r = np.linalg.norm(r_vec)
    v = np.linalg.norm(v_vec)
    h_vec = np.cross(r_vec, v_vec)
    h = np.linalg.norm(h_vec)
    k_vec = np.array([0.0, 0.0, 1.0])
    n_vec = np.cross(k_vec, h_vec)
    n = np.linalg.norm(n_vec)
    e_vec = (np.cross(v_vec, h_vec) / mu) - (r_vec / r)
    e = np.linalg.norm(e_vec)

    # inclination
    i = np.degrees(np.arccos(h_vec[2] / h))

    # RAAN
    if n > 1e-12:
        RAAN = np.degrees(np.arccos(n_vec[0] / n))
        if n_vec[1] < 0:
            RAAN = 360.0 - RAAN
    else:
        RAAN = 0.0

    # argument of perigee
    if n > 1e-12 and e > 1e-12:
        omega = np.degrees(np.arccos(np.dot(n_vec, e_vec) / (n * e)))
        if e_vec[2] < 0:
            omega = 360.0 - omega
    else:
        omega = 0.0

    # true anomaly
    if e > 1e-12:
        theta = np.degrees(np.arccos(np.dot(e_vec, r_vec) / (e * r)))
        if np.dot(r_vec, v_vec) < 0:
            theta = 360.0 - theta
    else:
        theta = 0.0

    # specific energy and semi-major axis
    eps = v**2 / 2.0 - mu / r
    a = -mu / (2.0 * eps)
    p = h**2 / mu

    return {
        'h': h,
        'e': e,
        'i_deg': i,
        'RAAN_deg': RAAN,
        'omega_deg': omega,
        'theta_deg': theta,
        'a_km': a,
        'p_km': p
    }

# Example: Problem 4.3
r_vec = np.array([2615.0, 15881.0, 3980.0])
v_vec = np.array([-2.767, -0.7905, 4.98])
print(orbital_elements(r_vec, v_vec))
```

---

If you want, I can:

* Export this as a downloadable `README.md` file,
* Add a 3D plot for each orbit (Matplotlib) and include the figure images in the README,
* Or compress the Python code into a small CLI script that reads vectors from a CSV.

Tell me which of these you'd like next!    creat readme file for this  
