
const flashcards = [
  { question: "What does HTML stand for?", answer: "HyperText Markup Language" },
  { question: "What is the purpose of CSS?", answer: "To style HTML content" },
  { question: "What does DOM stand for?", answer: "Document Object Model" },
  { question: "What does JS stand for?", answer: "JavaScript" },
  { question: "What is a function?", answer: "A reusable block of code" },
  { question: "What is an array?", answer: "A list of items" },
  { question: "What does API stand for?", answer: "Application Programming Interface" },
  { question: "What is a boolean?", answer: "True or false value" },
  { question: "What is NaN?", answer: "'Not-a-Number'" },
  { question: "What is 'null'?", answer: "An intentional absence of any value" },
];

const container = document.getElementById("flashcard-container");

flashcards.forEach((cardData) => {
  const card = document.createElement("div");
  card.classList.add("card");

  card.innerHTML = `
    <div class="card-inner">
      <div class="card-front">${cardData.question}</div>
      <div class="card-back">${cardData.answer}</div>
    </div>
  `;

  card.addEventListener("click", () => {
    card.classList.toggle("flipped");
  });

  container.appendChild(card);
});
