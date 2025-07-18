document.getElementById("attendanceForm").addEventListener("submit", function (e) {
  e.preventDefault();

  const date = document.getElementById("date").value;
  const inTime = document.getElementById("inTime").value;
  const outTime = document.getElementById("outTime").value;
  const overtime = document.getElementById("overtime").value || "0";
  const nightShift = document.getElementById("nightShift").value;

  const summary = `
    <strong>Date:</strong> ${date}<br>
    <strong>In Time:</strong> ${inTime}<br>
    <strong>Out Time:</strong> ${outTime}<br>
    <strong>Overtime:</strong> ${overtime} hrs<br>
    <strong>Night Shift:</strong> ${nightShift}
  `;

  document.getElementById("output").innerHTML = summary;
});
