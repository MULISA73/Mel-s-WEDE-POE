
// Mel's Cakes & Treats
// Scroll Reveal Animations

document.addEventListener("DOMContentLoaded", function () {

    // Select elements to animate
    const elements = document.querySelectorAll(
        ".content-card, .product-card, .faq-section"
    );

    // Add reveal class
    elements.forEach(function (element) {
        element.classList.add("reveal");
    });

    // Check browser support
    if ("IntersectionObserver" in window) {

        const observer = new IntersectionObserver(function (entries) {

            entries.forEach(function (entry) {

                if (entry.isIntersecting) {

                    entry.target.classList.add("visible");

                    observer.unobserve(entry.target);

                }

            });

        }, {
            threshold: 0.15
        });

        elements.forEach(function (element) {
            observer.observe(element);
        });

    } else {

        // Display elements normally in older browsers
        elements.forEach(function (element) {
            element.classList.add("visible");
        });

    }

});


document.addEventListener("DOMContentLoaded", function () {

   const form = document.getElementById("enquiryForm");
const formMessage = document.getElementById("formMessage");

if (!form || !formMessage) return;

const submitButton = form.querySelector('[type="submit"]');

    form.addEventListener("submit", async function (event) {

        event.preventDefault();

        if (!form.checkValidity()) {
            form.reportValidity();
            return;
        }

        submitButton.disabled = true;
        submitButton.value = "Sending...";
        formMessage.textContent = "Sending your enquiry...";

        try {
            const response = await fetch(form.action, {
                method: "POST",
                body: new FormData(form),
                headers: {
                    "Accept": "application/json"
                }
            });

            if (response.ok) {
                formMessage.textContent =
                    "Thank you! Your enquiry has been sent successfully.";

                formMessage.style.color = "#6f2849";
                form.reset();

            } else {
                formMessage.textContent =
                    "Sorry, we could not send your enquiry. Please try again.";
                formMessage.style.color = "red";
            }

        } catch (error) {
            formMessage.textContent =
                "A connection error occurred. Please try again.";
            formMessage.style.color = "red";
        }

        submitButton.disabled = false;
        submitButton.value = "Submit Quote Request";
    });

    form.addEventListener("reset", function () {
        formMessage.textContent = "";
    });

});

document.addEventListener("DOMContentLoaded", function () {

    const faqQuestions = document.querySelectorAll(".faq-question");

    faqQuestions.forEach(function (question) {

        question.addEventListener("click", function () {

            const answer = question.nextElementSibling;
            const icon = question.querySelector("span");

            const isOpen = question.getAttribute("aria-expanded") === "true";

            // Close all FAQ answers
            faqQuestions.forEach(function (item) {

                item.setAttribute("aria-expanded", "false");
                item.nextElementSibling.hidden = true;
                item.querySelector("span").textContent = "+";

            });

            // Open selected answer if it was previously closed
            if (!isOpen) {

                question.setAttribute("aria-expanded", "true");
                answer.hidden = false;
                icon.textContent = "-";

            }

        });

    });

});

document.addEventListener("DOMContentLoaded", function () {

    const productImages = document.querySelectorAll(".product-card img");

    // Create the lightbox
    const lightbox = document.createElement("div");
    lightbox.id = "imageLightbox";
    lightbox.className = "lightbox";

    lightbox.innerHTML = `
        <button class="lightbox-close" aria-label="Close image">&times;</button>
        <img class="lightbox-image" src="" alt="">
        <p class="lightbox-caption"></p>
    `;

    document.body.appendChild(lightbox);

    const enlargedImage = lightbox.querySelector(".lightbox-image");
    const caption = lightbox.querySelector(".lightbox-caption");
    const closeButton = lightbox.querySelector(".lightbox-close");

    // Open image when clicked
    productImages.forEach(function (image) {

        image.style.cursor = "pointer";

        image.addEventListener("click", function () {

            enlargedImage.src = image.src;
            enlargedImage.alt = image.alt;
            caption.textContent = image.alt;

            lightbox.classList.add("active");
            document.body.style.overflow = "hidden";

            closeButton.focus();
        });

    });

    // Close lightbox
    function closeLightbox() {
        lightbox.classList.remove("active");
        document.body.style.overflow = "";
    }

    closeButton.addEventListener("click", closeLightbox);

    // Close when clicking outside the image
    lightbox.addEventListener("click", function (event) {
        if (event.target === lightbox) {
            closeLightbox();
        }
    });

    // Close using Escape key
    document.addEventListener("keydown", function (event) {
        if (event.key === "Escape" && lightbox.classList.contains("active")) {
            closeLightbox();
        }
    });

});

document.addEventListener("DOMContentLoaded", function () {

    const menuToggle = document.getElementById("menuToggle");
    const mainNavigation = document.getElementById("mainNavigation");

    if (!menuToggle || !mainNavigation) return;

    menuToggle.addEventListener("click", function () {

        const isOpen = mainNavigation.classList.toggle("active");

        menuToggle.setAttribute("aria-expanded", isOpen);

        menuToggle.setAttribute(
            "aria-label",
            isOpen ? "Close navigation menu" : "Open navigation menu"
        );

    });

    const navigationLinks = mainNavigation.querySelectorAll("a");

    navigationLinks.forEach(function (link) {

        link.addEventListener("click", function () {
            mainNavigation.classList.remove("active");
            menuToggle.setAttribute("aria-expanded", "false");
            menuToggle.setAttribute("aria-label", "Open navigation menu");
        });

    });

});

// Product Search and Filtering

document.addEventListener("DOMContentLoaded", function () {

    const searchInput = document.getElementById("productSearch");
    const categoryFilter = document.getElementById("categoryFilter");
    const productCards = document.querySelectorAll(".product-card");
    const productCount = document.getElementById("productCount");
    const noProducts = document.getElementById("noProducts");

    function filterProducts() {

        const searchText = searchInput.value.toLowerCase().trim();
        const selectedCategory = categoryFilter.value;

        let visibleProducts = 0;

        productCards.forEach(function (card) {

            const productName = card.querySelector("h2").textContent.toLowerCase();
            const productDescription = card.querySelector(".product-card-content p").textContent.toLowerCase();
            const productCategory = card.dataset.category;

            const matchesSearch =
                productName.includes(searchText) ||
                productDescription.includes(searchText);

            const matchesCategory =
                selectedCategory === "all" ||
                productCategory === selectedCategory;

            if (matchesSearch && matchesCategory) {
                card.style.display = "";
                visibleProducts++;
            } else {
                card.style.display = "none";
            }

        });

        productCount.textContent =
            "Showing " + visibleProducts + " of " + productCards.length + " products";

        noProducts.hidden = visibleProducts !== 0;
    }

    searchInput.addEventListener("input", filterProducts);
    categoryFilter.addEventListener("change", filterProducts);

});
