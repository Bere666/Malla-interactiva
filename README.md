# Malla-interactiva
// script.js

const malla = [
  {
    semestre: "Primer Semestre",
    ramos: [
      { nombre: "Administración", tipo: "anual" },
      { nombre: "Economía", tipo: "anual" },
      { nombre: "Matemática", tipo: "anual" },
      { nombre: "Comunicación Oral y Escrita I", tipo: "semestral" },
      { nombre: "Idioma Extranjero I", tipo: "semestral" },
      { nombre: "Introducción a la Carrera", tipo: "semestral" },
      { nombre: "Fundamentos de Contabilidad", tipo: "semestral" }
    ]
  },
  {
    semestre: "Segundo Semestre",
    ramos: [
      { nombre: "Comunicación Oral y Escrita II", tipo: "semestral", prereq: ["Comunicación Oral y Escrita I"] },
      { nombre: "Idioma Extranjero II", tipo: "semestral", prereq: ["Idioma Extranjero I"] },
      { nombre: "Sistema de Información Contable", tipo: "semestral", prereq: ["Fundamentos de Contabilidad"] }
    ]
  },
  // Agrega aquí los semestres 3 al 11 y extras como deporte si se desea
];

const container = document.getElementById("malla-container");

malla.forEach(({ semestre, ramos }) => {
  const div = document.createElement("div");
  div.classList.add("semestre");

  const title = document.createElement("h2");
  title.textContent = semestre;
  div.appendChild(title);

  ramos.forEach(({ nombre }) => {
    const ramoDiv = document.createElement("div");
    ramoDiv.classList.add("ramo");
    ramoDiv.textContent = nombre;
    ramoDiv.addEventListener("click", () => {
      ramoDiv.classList.toggle("aprobado");
    });
    div.appendChild(ramoDiv);
  });

  container.appendChild(div);
});
