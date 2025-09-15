<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Arbeitsende-Rechner</title>

  <!-- Bootstrap 5.x CSS (5.3.3 CDN als stabile 5er-Version) -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">

  <style>
    :root {
      --card-max-width: 980px;
    }
    body {
      background: #0b0c10;
      color: #eaf0f1;
    }
    .page-wrap {
      padding: 2rem 1rem 4rem;
    }
    .app-card {
      background: #111318;
      border: 1px solid #232733;
      box-shadow: 0 8px 24px rgba(0,0,0,0.35);
      border-radius: 1rem;
      max-width: var(--card-max-width);
      margin: 0 auto;
    }
    .form-section-title {
      font-weight: 600;
      color: #9ecbff;
      letter-spacing: .2px;
      margin-bottom: .25rem;
    }
    .subtle {
      color: #aab3c2;
      font-size: .925rem;
    }
    .result-kpi {
      background: #0f1420;
      border: 1px solid #1f2a3a;
      border-radius: .75rem;
      padding: 1rem;
      height: 100%;
    }
    .kpi-label {
      font-size: .875rem;
      color: #b7c3d5;
      margin-bottom: .25rem;
    }
    .kpi-value {
      font-size: 1.5rem;
      font-weight: 700;
      color: #ffffff;
    }
    .divider {
      height: 1px;
      background: linear-gradient(90deg, transparent, #2a3447, transparent);
      margin: 1rem 0 1.25rem;
    }
    .invalid-feedback {
      display: block; /* Sofort unter dem Feld sichtbar, wenn Fehlertext gesetzt wird */
    }
    .list-checks .list-group-item {
      background: transparent;
      color: #eaf0f1;
      border-color: #263044;
    }
    .list-checks .badge {
      background: #22314a;
      border: 1px solid #2e4368;
    }
    .muted {
      color: #98a3b6;
    }
    .foot-note {
      font-size: .85rem;
      color: #8ea0b8;
    }
    .brand {
      font-weight: 700;
      letter-spacing: .3px;
      color: #ffffff;
    }
    a, a:hover { color: #9ecbff; }
    .btn-primary {
      background: #2c66f5;
      border-color: #2c66f5;
    }
    .btn-outline-light {
      color: #eaf0f1;
      border-color: #445168;
    }
    .btn-outline-light:hover {
      background: #1a2233;
    }
    /* Consent-Box */
    .consent-box {
      background: #0f1420;
      border: 1px solid #1f2a3a;
      border-radius: .75rem;
      padding: 1rem;
    }
  </style>
</head>
<body>
  <div class="page-wrap">
    <div class="container">
      <header class="mb-4 text-center">
        <h1 class="brand">Arbeitsende-Rechner</h1>
        <p class="subtle mb-0">Berechnet deine Abfahrtszeit (Arbeitsende) basierend auf Fahrzeit, Arbeitsbeginn, geplanter Gesamtarbeitszeit und gesetzlichen Pausen.</p>
      </header>

      <div class="app-card p-4 p-md-5">
        <!-- Formular -->
        <form id="calcForm" novalidate>
          <!-- Sektion 1: Fahrt -->
          <div class="mb-4">
            <div class="form-section-title">1) An- / Abfahrt</div>
            <p class="subtle">Gib an, wann du zuhause losgefahren und angekommen bist. Wähle, ob du alleine oder zu zweit gefahren bist.</p>

            <div class="row g-3 align-items-end">
              <div class="col-md-4">
                <label for="homeDeparture" class="form-label">1.1 Abfahrt zuhause</label>
                <input type="time" class="form-control" id="homeDeparture" required step="60" />
                <div class="invalid-feedback" id="homeDepartureError"></div>
              </div>
              <div class="col-md-4">
                <label for="arrivalWork" class="form-label">1.1 Ankunft am Arbeitsplatz</label>
                <input type="time" class="form-control" id="arrivalWork" required step="60" />
                <div class="invalid-feedback" id="arrivalWorkError"></div>
              </div>
              <div class="col-md-4">
                <label for="driverMode" class="form-label">1.2 Fahrmodus</label>
                <select id="driverMode" class="form-select">
                  <option value="solo">Alleinfahrer</option>
                  <option value="shared">Zu zweit (Fahrzeit / 2)</option>
                </select>
              </div>
            </div>
          </div>

          <div class="divider"></div>

          <!-- Sektion 2: Arbeit -->
          <div class="mb-4">
            <div class="form-section-title">2) Arbeitstag</div>
            <p class="subtle">Wähle deinen Arbeitsbeginn und die geplante Gesamtarbeitszeit. Pausen nach ArbZG werden automatisch berücksichtigt und angezeigt. Die Fahrzeit aus (1) wird von der Gesamtarbeitszeit abgezogen.</p>

            <!-- FIX: align-items-start statt align-items-end -->
            <div class="row g-3 align-items-start">
              <div class="col-md-4">
                <label for="workStart" class="form-label">2.1 Arbeitsbeginn</label>
                <input type="time" class="form-control" id="workStart" required step="60" />
                <div class="invalid-feedback" id="workStartError"></div>
              </div>
              <div class="col-md-8">
                <label for="plannedWork" class="form-label">2.2 Geplante Gesamtarbeitszeit</label>
                <select id="plannedWork" class="form-select">
                  <option value="6">6:00 h</option>
                  <option value="7">7:00 h</option>
                  <option value="8" selected>8:00 h</option>
                  <option value="9">9:00 h</option>
                  <option value="10">10:00 h</option>
                  <option value="11">11:00 h</option>
                  <option value="12">12:00 h</option>
                </select>
                <div class="form-text text-muted muted">
                  Pausenregel (DE): bis 6:00 h → 0 Min, &gt;6:00–9:00 h → 30 Min, &gt;9:00 h → 45 Min.
                </div>
              </div>

              <!-- NEU: Pausen-Basis (Fahrzeit einbeziehen?) -->
              <div class="col-12">
                <label for="breakTravelMode" class="form-label">2.3 Fahrzeit in Pausenberechnung berücksichtigen?</label>
                <select id="breakTravelMode" class="form-select">
                  <option value="no" selected>Nein – Pause nur ab Arbeitsbeginn (Fahrzeit NICHT mitzählen)</option>
                  <option value="yes">Ja – Fahrzeit als Arbeitszeit mitzählen (Pausenpflicht kann höher sein)</option>
                </select>
                <div class="form-text text-muted muted">
                  Steuert, ob die gesetzliche Pausenpflicht auf Grundlage der gesamten geplanten Arbeitszeit (inkl. Fahrzeit) oder nur der Zeit ab Arbeitsbeginn ermittelt wird.
                </div>
              </div>
            </div>
          </div>

          <div class="divider"></div>

          <!-- Aktionen -->
          <div class="d-flex gap-2 flex-wrap">
            <button type="button" id="btnCalculate" class="btn btn-primary">
              Berechnen
            </button>
            <button type="reset" id="btnReset" class="btn btn-outline-light">
              Zurücksetzen
            </button>
          </div>
        </form>

        <div class="divider"></div>

        <!-- Ergebnisse -->
        <section aria-live="polite" aria-atomic="true">
          <h2 class="h5 mb-3">Ergebnisse</h2>

          <div class="row g-3">
            <div class="col-md-4">
              <div class="result-kpi">
                <div class="kpi-label">Fahrdauer (brutto)</div>
                <div class="kpi-value" id="driveDuration">–</div>
                <div class="muted">Aus Ankunft − Abfahrt (ggf. über Mitternacht).</div>
              </div>
            </div>
            <div class="col-md-4">
              <div class="result-kpi">
                <div class="kpi-label">Fahrdauer angerechnet</div>
                <div class="kpi-value" id="driveCredited">–</div>
                <div class="muted">Bei „Zu zweit“ halbiert.</div>
              </div>
            </div>
            <div class="col-md-4">
              <div class="result-kpi">
                <div class="kpi-label">Pausen gesamt</div>
                <div class="kpi-value" id="breakTotal">–</div>
                <div class="muted">Gemäß geplanter Gesamtarbeitszeit bzw. Einstellung 2.3.</div>
              </div>
            </div>
          </div>

          <div class="row g-3 mt-1">
            <div class="col-md-6">
              <div class="result-kpi h-100">
                <div class="kpi-label">Abfahrtszeit (Arbeitsende)</div>
                <div class="kpi-value" id="workEnd">–</div>
                <div class="muted">
                  Formel: Arbeitsbeginn + (Gesamtarbeitszeit − angerechnete Fahrzeit) + Pausen.
                </div>
              </div>
            </div>
            <div class="col-md-6">
              <div class="result-kpi h-100">
                <div class="kpi-label">Pausen-Details</div>
                <ul class="list-group list-group-flush list-checks" id="breakDetails">
                  <li class="list-group-item d-flex justify-content-between align-items-center">
                    <span class="muted">Noch keine Auswahl</span>
                    <span class="badge text-bg-secondary">–</span>
                  </li>
                </ul>
              </div>
            </div>
          </div>

          <p class="foot-note mt-3 mb-3">
            2.3: Die Pausenpflicht kann wahlweise mit oder ohne Fahrzeit ermittelt werden. Die Fahrzeit wird weiterhin vollständig von der <em>geplanten</em> Gesamtarbeitszeit abgezogen (bei „Zu zweit“ halbiert), um die Nettozeit im Betrieb zu bestimmen.
          </p>

          <!-- Consent: Cookies speichern -->
          <div class="consent-box">
            <div class="form-check">
              <input class="form-check-input" type="checkbox" id="cookieConsent">
              <label class="form-check-label" for="cookieConsent">
                Cookies erlauben (Eingaben speichern)
              </label>
            </div>
            <p class="muted mb-0 mt-2">
              Wenn aktiviert, speichert diese Seite deine Formularwerte für max. 180 Tage in Funktions-Cookies (<code>SameSite=Lax</code>, keine Drittanbieter-/Tracking-Cookies).
              Du kannst die Speicherung jederzeit über das Häkchen wieder deaktivieren.
            </p>
          </div>
        </section>
      </div>
    </div>
  </div>

  <!-- Bootstrap 5.x JS (Bundle inkl. Popper) -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"
          integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz"
          crossorigin="anonymous"></script>

  <script>
    // -------------------------------
    // Cookie-Helfer
    // -------------------------------
    function setCookie(name, value, days) {
      const expires = new Date(Date.now() + days * 864e5).toUTCString();
      document.cookie = name + "=" + encodeURIComponent(value) + "; expires=" + expires + "; path=/; SameSite=Lax";
    }
    function getCookie(name) {
      const match = document.cookie.split("; ").find(row => row.startsWith(name + "="));
      return match ? decodeURIComponent(match.split("=")[1]) : null;
    }
    function deleteCookie(name) {
      document.cookie = name + "=; Max-Age=0; path=/; SameSite=Lax";
    }

    const CONSENT_COOKIE = "arbeitsendeConsent";
    const PREFS_COOKIE   = "arbeitsendePrefs";
    const COOKIE_TTL_DAYS = 180;

    function hasConsent() {
      return getCookie(CONSENT_COOKIE) === "1";
    }
    function setConsent(allowed) {
      setCookie(CONSENT_COOKIE, allowed ? "1" : "0", COOKIE_TTL_DAYS);
      if (!allowed) {
        deleteCookie(PREFS_COOKIE);
      }
    }

    function savePrefs() {
      if (!hasConsent()) return;
      const prefs = {
        homeDeparture: document.getElementById("homeDeparture").value || "",
        arrivalWork:   document.getElementById("arrivalWork").value   || "",
        driverMode:    document.getElementById("driverMode").value    || "solo",
        workStart:     document.getElementById("workStart").value     || "",
        plannedWork:   document.getElementById("plannedWork").value   || "8",
        breakTravelMode: document.getElementById("breakTravelMode").value || "no"
      };
      try {
        setCookie(PREFS_COOKIE, JSON.stringify(prefs), COOKIE_TTL_DAYS);
      } catch (e) {
        // Fallback: wenn JSON oder Größe fehlschlägt, Cookie leeren
        deleteCookie(PREFS_COOKIE);
      }
    }

    function loadPrefs() {
      const raw = getCookie(PREFS_COOKIE);
      if (!raw) return;
      try {
        const prefs = JSON.parse(raw);
        if (prefs && typeof prefs === "object") {
          if (prefs.homeDeparture) document.getElementById("homeDeparture").value = prefs.homeDeparture;
          if (prefs.arrivalWork)   document.getElementById("arrivalWork").value   = prefs.arrivalWork;
          if (prefs.driverMode)    document.getElementById("driverMode").value    = prefs.driverMode;
          if (prefs.workStart)     document.getElementById("workStart").value     = prefs.workStart;
          if (prefs.plannedWork)   document.getElementById("plannedWork").value   = prefs.plannedWork;
          if (prefs.breakTravelMode) document.getElementById("breakTravelMode").value = prefs.breakTravelMode;
        }
      } catch (e) {
        // Ungültiger Inhalt → Cookie löschen
        deleteCookie(PREFS_COOKIE);
      }
    }

    // -------------------------------
    // Hilfsfunktionen für Zeit & Dauer
    // -------------------------------

    /**
     * Parst einen "HH:MM"-String zu Minuten seit 00:00.
     * @param {string} hhmm
     * @returns {number|null}
     */
    function parseHHMMToMinutes(hhmm) {
      if (!hhmm || !/^\d{2}:\d{2}$/.test(hhmm)) return null;
      const [h, m] = hhmm.split(":").map(Number);
      if (h > 23 || m > 59) return null;
      return h * 60 + m;
    }

    /**
     * Formatiert Minuten (>= 0) nach "HH:MM".
     * @param {number} minutes
     * @returns {string}
     */
    function formatMinutesToHHMM(minutes) {
      // Normalisiere ins 24h-Fenster, aber merke auch Tage > 0
      const days = Math.floor(Math.max(0, minutes) / (24 * 60));
      const rem = ((minutes % (24 * 60)) + (24 * 60)) % (24 * 60);
      const hh = String(Math.floor(rem / 60)).padStart(2, "0");
      const mm = String(rem % 60).padStart(2, "0");
      return days > 0 ? `${hh}:${mm} (+${days}d)` : `${hh}:${mm}`;
    }

    /**
     * Formatiert eine Dauer in "H:MM h".
     * @param {number} minutes
     * @returns {string}
     */
    function formatDuration(minutes) {
      const sign = minutes < 0 ? "-" : "";
      const abs = Math.abs(Math.round(minutes));
      const h = Math.floor(abs / 60);
      const m = abs % 60;
      return `${sign}${h}:${String(m).padStart(2, "0")} h`;
    }

    /**
     * Differenz zwischen zwei Zeiten in Minuten (über Mitternacht möglich).
     * @param {string} startHHMM
     * @param {string} endHHMM
     * @returns {number|null}
     */
    function diffMinutesOverMidnight(startHHMM, endHHMM) {
      const s = parseHHMMToMinutes(startHHMM);
      const e = parseHHMMToMinutes(endHHMM);
      if (s == null || e == null) return null;
      let d = e - s;
      if (d < 0) d += 24 * 60; // über Mitternacht
      return d;
    }

    // -------------------------------
    // Pausenregel (DE ArbZG – vereinfachtes Modell)
    // -------------------------------
    function getBreakMinutesForPlannedHours(hours) {
      // Stunden → Minuten gesetzliche Pausen (vereinfachte Standardregel)
      // <= 6: 0, >6 bis 9: 30, >9: 45
      const h = Number(hours);
      if (h <= 6) return 0;
      if (h <= 9) return 30;
      return 45;
    }

    function getBreakDetails(hours) {
      const total = getBreakMinutesForPlannedHours(hours);
      const details = [];
      if (total === 0) {
        details.push({ label: "Keine Pause erforderlich", minutes: 0 });
      } else if (total === 30) {
        details.push({ label: "Pflichtpause", minutes: 30 });
      } else if (total === 45) {
        details.push({ label: "Pflichtpause", minutes: 45 });
      }
      return { total, details };
    }

    // -------------------------------
    // Validierung
    // -------------------------------
    function setError(el, msg) {
      el.classList.add("is-invalid");
      el.classList.remove("is-valid");
      const fb = el.nextElementSibling;
      if (fb && fb.classList.contains("invalid-feedback")) {
        fb.textContent = msg || "";
      }
    }
    function clearError(el) {
      el.classList.remove("is-invalid");
      if (el.value) el.classList.add("is-valid");
      const fb = el.nextElementSibling;
      if (fb && fb.classList.contains("invalid-feedback")) {
        fb.textContent = "";
      }
    }

    // -------------------------------
    // Hauptberechnung
    // -------------------------------
    function calculate() {
      const homeDepartureEl = document.getElementById("homeDeparture");
      const arrivalWorkEl   = document.getElementById("arrivalWork");
      const driverModeEl    = document.getElementById("driverMode");
      const workStartEl     = document.getElementById("workStart");
      const plannedWorkEl   = document.getElementById("plannedWork");
      const breakTravelModeEl = document.getElementById("breakTravelMode");

      // Ergebnis-Elemente
      const driveDurationEl = document.getElementById("driveDuration");
      const driveCreditedEl = document.getElementById("driveCredited");
      const breakTotalEl    = document.getElementById("breakTotal");
      const breakDetailsEl  = document.getElementById("breakDetails");
      const workEndEl       = document.getElementById("workEnd");

      // Eingaben prüfen
      let valid = true;

      const homeDeparture = homeDepartureEl.value;
      const arrivalWork   = arrivalWorkEl.value;
      const workStart     = workStartEl.value;
      const plannedHrs    = Number(plannedWorkEl.value);
      const driverMode    = driverModeEl.value;
      const breakTravelMode = breakTravelModeEl.value; // "yes" | "no"

      if (!homeDeparture) { setError(homeDepartureEl, "Bitte Abfahrtszeit eingeben."); valid = false; } else { clearError(homeDepartureEl); }
      if (!arrivalWork)   { setError(arrivalWorkEl,   "Bitte Ankunftszeit eingeben.");  valid = false; } else { clearError(arrivalWorkEl); }
      if (!workStart)     { setError(workStartEl,     "Bitte Arbeitsbeginn eingeben."); valid = false; } else { clearError(workStartEl); }

      if (!valid) {
        // Setze Anzeigen zurück
        driveDurationEl.textContent = "–";
        driveCreditedEl.textContent = "–";
        breakTotalEl.textContent = "–";
        workEndEl.textContent = "–";
        breakDetailsEl.innerHTML = `
          <li class="list-group-item d-flex justify-content-between align-items-center">
            <span class="muted">Eingaben unvollständig</span>
            <span class="badge text-bg-secondary">–</span>
          </li>`;
        // Bei Änderungen trotzdem evtl. speichern (z.B. unvollständig), damit beim Reload die bisherigen Eingaben da sind
        savePrefs();
        return;
      }

      // 1) Fahrzeit brutto
      const driveMinutes = diffMinutesOverMidnight(homeDeparture, arrivalWork);
      if (driveMinutes == null) {
        setError(homeDepartureEl, "Ungültige Zeit.");
        setError(arrivalWorkEl, "Ungültige Zeit.");
        savePrefs();
        return;
      }

      // 1.2) Fahrzeit angerechnet (ggf. halbiert)
      const creditedDrive = driverMode === "shared" ? driveMinutes / 2 : driveMinutes;

      // 2) Netto-Arbeitszeit im Betrieb = geplante Stunden − angerechnete Fahrzeit
      const plannedTotalMin = plannedHrs * 60;
      const netWorkAtSite = plannedTotalMin - creditedDrive;
      const netClamped = Math.max(0, netWorkAtSite);

      // 3) Pausenpflicht-BASIS nach Einstellung 2.3
      //    - "yes"  → Basis = geplante Gesamtarbeitszeit (inkl. Fahrzeit)
      //    - "no"   → Basis = geplante Gesamtarbeitszeit minus angerechnete Fahrzeit (ab Arbeitsbeginn)
      const breakBasisMin = Math.max(0, breakTravelMode === "yes" ? plannedTotalMin : plannedTotalMin - creditedDrive);
      const breakBasisHours = breakBasisMin / 60;

      // 4) Pausen gem. Basis-Stunden
      const { total: breakMinutes, details } = getBreakDetails(breakBasisHours);

      // Endzeit = Arbeitsbeginn + Nettozeit + Pausen
      const workStartMin = parseHHMMToMinutes(workStart);
      if (workStartMin == null) {
        setError(workStartEl, "Ungültige Zeit.");
        savePrefs();
        return;
      }
      const endMinutesAbs = workStartMin + netClamped + breakMinutes;

      // Ausgabe
      driveDurationEl.textContent = formatDuration(driveMinutes);
      driveCreditedEl.textContent = formatDuration(creditedDrive);
      breakTotalEl.textContent    = formatDuration(breakMinutes);
      workEndEl.textContent       = formatMinutesToHHMM(endMinutesAbs);

      // Pausen-Detailsliste
      const basisLabel = breakTravelMode === "yes"
        ? "Basis für Pausen (inkl. Fahrzeit)"
        : "Basis für Pausen (ab Arbeitsbeginn)";

      const basisItem = `
        <li class="list-group-item d-flex justify-content-between align-items-center">
          <span class="muted">${basisLabel}</span>
          <span class="badge text-bg-secondary">${formatDuration(breakBasisMin).replace(" h","")}</span>
        </li>`;

      if (details.length === 0) {
        breakDetailsEl.innerHTML = `
          ${basisItem}
          <li class="list-group-item d-flex justify-content-between align-items-center">
            <span>Keine Pause erforderlich</span>
            <span class="badge text-bg-secondary">0 Min</span>
          </li>`;
      } else {
        breakDetailsEl.innerHTML = basisItem + details.map(d => `
          <li class="list-group-item d-flex justify-content-between align-items-center">
            <span>${d.label}</span>
            <span class="badge text-bg-secondary">${d.minutes} Min</span>
          </li>
        `).join("");
      }

      // Nach erfolgreicher Berechnung/Änderung speichern (falls erlaubt)
      savePrefs();
    }

    // -------------------------------
    // Event-Listener
    // -------------------------------
    document.getElementById("btnCalculate").addEventListener("click", calculate);

    // Live-Berechnung bei Änderungen + Speichern
    ["homeDeparture","arrivalWork","driverMode","workStart","plannedWork","breakTravelMode"].forEach(id => {
      const el = document.getElementById(id);
      el.addEventListener("change", calculate);
      el.addEventListener("input", calculate);
    });

    // Reset-Button
    document.getElementById("btnReset").addEventListener("click", () => {
      // kleine Verzögerung, damit die Felder wirklich geleert sind
      setTimeout(() => {
        // Gültigkeitsklassen entfernen
        ["homeDeparture","arrivalWork","driverMode","workStart","plannedWork","breakTravelMode"].forEach(id => {
          const el = document.getElementById(id);
          el.classList.remove("is-valid","is-invalid");
        });
        // Ergebnisse leeren
        document.getElementById("driveDuration").textContent = "–";
        document.getElementById("driveCredited").textContent = "–";
        document.getElementById("breakTotal").textContent = "–";
        document.getElementById("workEnd").textContent = "–";
        document.getElementById("breakDetails").innerHTML = `
          <li class="list-group-item d-flex justify-content-between align-items-center">
            <span class="muted">Noch keine Auswahl</span>
            <span class="badge text-bg-secondary">–</span>
          </li>`;

        // Nach Reset ggf. auch speichern (leere Werte), falls Consent aktiv
        savePrefs();
      }, 0);
    });

    // Consent-Checkbox Verhalten
    const consentEl = document.getElementById("cookieConsent");
    consentEl.addEventListener("change", () => {
      const allowed = consentEl.checked;
      setConsent(allowed);
      if (allowed) {
        // Sofort aktuelle Werte sichern
        savePrefs();
      } else {
        // Cookies gelöscht → nichts weiter zu tun
      }
    });

    // Initiale Wiederherstellung & Berechnung
    window.addEventListener("DOMContentLoaded", () => {
      // Consent-Status aus Cookie in Checkbox spiegeln
      consentEl.checked = hasConsent();

      // Falls erlaubt, Prefs laden
      if (hasConsent()) {
        loadPrefs();
      }

      // Initial berechnen (falls Browser Defaultwerte setzt oder Prefs geladen wurden)
      calculate();
    });
  </script>
</body>
</html>
