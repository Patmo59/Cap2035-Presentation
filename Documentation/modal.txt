const modal = document.querySelector(".modal");/*contenu*/
const btnModal = document.querySelector(".btn-modal");/*btn description*/
const close = document.querySelector(".close-modal");/*btnFermer*/
const overlay = document.querySelector(".overlay");
if(modal){
  btnModal.addEventListener("click", () => {
    modal.style.display = "block";
    overlay.style.display = "block";
  });
  /*ferme la box */
  close.addEventListener("click", closeModal);
  modal.addEventListener("click", (event) => {
    if (event.target == modal) {
      console.log(event.target == modal);
      closeModal();
    }
  });
}

function closeModal() {
  modal.style.display = "none";
  overlay.style.display = "none";
}
//========Nav bar=============
const connect =document.querySelector(".btnconnect");
const deconnect =document.querySelector(".btndeconnect");
  connect.addEventListener("click", () => { 
     window.location.assign("/connexion");
});
deconnect.addEventListener("click", ()=> {
  window.location.assign("/deconnexion");
})