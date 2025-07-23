# Malla-interactiva
/* style.css */

body {
  font-family: 'Segoe UI', sans-serif;
  background-color: #fefdfd;
  color: #333;
  margin: 0;
  padding: 20px;
}

h1 {
  text-align: center;
  color: #6b5b95;
}

#malla-container {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 1rem;
  margin-top: 20px;
}

.semestre {
  background-color: #f6f1f7;
  border-left: 5px solid #b39ddb;
  border-radius: 10px;
  padding: 10px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

.semestre h2 {
  margin-top: 0;
  color: #5e548e;
}

.ramo {
  background-color: #fff;
  margin: 5px 0;
  padding: 10px;
  border: 2px solid #d1c4e9;
  border-radius: 8px;
  cursor: pointer;
  transition: background-color 0.3s, border-color 0.3s;
}

.ramo:hover {
  background-color: #ede7f6;
}

.ramo.aprobado {
  background-color: #c8e6c9;
  border-color: #66bb6a;
  text-decoration: line-through;
}
