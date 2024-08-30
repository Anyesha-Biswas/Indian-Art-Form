const timelineItems = [
    {
        id: 1,
        period: "Indus Valley Civilization (3300-1300 BCE)",
        artifact: "Seal with Unicorn",
        image: "https://drive.google.com/uc?id=1QWERTYUIOPasdfghjkl", // Replace with your public image link
        description: "This seal features a unicorn-like creature and is one of the most famous artifacts from the Indus Valley Civilization."
    },
    {
        id: 2,
        period: "Mauryan Empire (322-185 BCE)",
        artifact: "Lion Capital of Ashoka",
        image: "https://drive.google.com/uc?id=2ZXCVBNMASDFGHJKL", // Replace with your public image link
        description: "The Lion Capital of Ashoka is a symbol of Indian sovereignty and features four lions standing back to back."
    },
    // Add more timeline items here
];

// Get the timeline container
const timelineContainer = document.querySelector('.timeline ul');

// Create a function to generate timeline items
function generateTimelineItems() {
    timelineItems.forEach((item) => {
        const timelineItem = document.createElement('li');
        timelineItem.innerHTML = `
            <img src="${item.image}" alt="${item.artifact}">
            <div class="info">
                <h2>${item.artifact}</h2>
                <p>${item.period}</p>
            </div>
        `;
        timelineItem.addEventListener('click', () => {
            showModal(item);
        });
        timelineContainer.appendChild(timelineItem);
    });
}

// Create a function to show the modal
function showModal(item) {
    const modal = document.getElementById('modal');
    const modalTitle = document.getElementById('modal-title');
    const modalDescription = document.getElementById('modal-description');
    const modalImage = document.getElementById('modal-image');
    const modalPeriod = document.getElementById('modal-period');

    modal.style.display = 'block';
    modalTitle.textContent = item.artifact;
    modalDescription.textContent = item.description;
    modalImage.src = item.image;
    modalPeriod.textContent = item.period;

    // Add an event listener to close the modal
    document.getElementById('close').addEventListener('click', () => {
        modal.style.display = 'none';
    });
}

// Generate the timeline items
generateTimelineItems();
