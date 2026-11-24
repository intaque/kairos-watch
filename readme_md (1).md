# ⏳ Kairos — World Clock & Timezone Explorer

**Kairos** is a modern, minimalist web application designed for seamlessly tracking time across multiple global cities and time zones. Named after the ancient Greek concept of *Kairos* (signifying the opportune, qualitative moment of time), this app combines aesthetic minimalism with precise timekeeping functionality.

## 🌐 Live Demo

Try the live application here:

👉 [**https://intaque.github.io/kairos-watch/**](https://intaque.github.io/kairos-watch/)

## ✨ Key Features

* **Real-Time Live Clock:** High-precision digital display showing hours, minutes, and seconds in real-time.
* **12h / 24h Format Switcher:** Toggle between 12-hour (AM/PM) and 24-hour time notation with a single click.
* **Global City Finder:** Search and inspect local time, city attributes, and timezone identifiers across world regions.
* **GMT / UTC Offset Tracker:** Displays the Greenwich Mean Time (GMT) differential relative to Coordinated Universal Time (UTC).
* **Minimalist Luxury Aesthetic:** High-contrast typography and clutter-free interface inspired by modern horology design.
* **Responsive Design:** Optimized layout for desktop monitors, tablets, and mobile smartphones.

## 📐 Time Conversion & GMT Mechanics

The time displayed for any selected global location is computed relative to UTC standard time using the city's GMT offset:

$$
T_{\text{city}} = T_{\text{UTC}} + \Delta t_{\text{GMT}}
$$

Where:

* $T_{\text{city}}$: Local calculated time for the selected city
* $T_{\text{UTC}}$: Current Coordinated Universal Time derived from system epoch $t_{\text{epoch}}$
* $\Delta t_{\text{GMT}}$: Standard offset in hours including daylight saving adjustments ($\text{DST}$)

### 12-Hour vs 24-Hour Conversion

For a given 24-hour hour index $H_{24} \in [0, 23]$:

$$
H_{12} = \begin{cases} 
12 & \text{if } H_{24} = 0 \text{ or } H_{24} = 12 \\ 
H_{24} \bmod 12 & \text{otherwise} 
\end{cases}
$$

$$
\text{Period} = \begin{cases} 
\text{AM} & \text{if } H_{24} < 12 \\ 
\text{PM} & \text{if } H_{24} \ge 12 
\end{cases}
$$

## 🛠️ Tech Stack

* **Frontend:** HTML5, CSS3, Modern Vanilla JavaScript (ES6+)
* **Styling:** Custom CSS Flexbox/Grid with typographic scaling
* **Hosting:** GitHub Pages

## 💻 Local Development Setup

To run Kairos locally on your machine:

1. **Clone the repository:**

   ```bash
   git clone https://github.com/intaque/kairos-watch.git
   cd kairos-watch
   ```

2. **Launch locally:**

   * Open `index.html` directly in your web browser, or use a local dev server such as Live Server in VS Code or `npx serve`.

   ```bash
   npx serve .
   ```

## 🤝 Contributing

Contributions, bug reports, and feature requests are welcome! Feel free to open an issue or submit a pull request on the GitHub repository.

## 📜 License

This project is open-source under the [MIT License](LICENSE).