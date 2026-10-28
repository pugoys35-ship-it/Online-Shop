<script>
import Navbar from './components/Navbar.vue'
import Home from './components/Home.vue'
import FeaturedProducts from './components/FeaturedProducts.vue'
import Footer from './components/Footer.vue'
import Products from './components/Products.vue';
import CartItem from './components/CartItem.vue';
import CheckOutForm from './components/CheckOutForm.vue';
import ProductsDetailsModal from './components/ProductsDetailsModal.vue';
import ConfirmationModal from './components/ConfirmationModal.vue';
import OrderHistory from './components/OrderHistory.vue';


export default {
  components: {
    Navbar,
    Home,
    FeaturedProducts,
    Products,
    CartItem,
    OrderHistory,
    ProductsDetailsModal,
    ConfirmationModal,
    Footer,
    CheckOutForm,
  },
  data() {
    return {
      productsElectronics: [

        { id: 1, name: 'Camera', image: 'https://i.pinimg.com/1200x/25/d9/83/25d9833b64439bcab819618ce496862b.jpg', price: 750, description: '33MP full-frame Exmor R back-illuminated CMOS sensor 8x more powerful, next generation BIONZ XR image processing engine Up to 4K 60p 10-bit 4:2:2 w/ full pixel readout in all recording formats 7K oversampling full-frame 4K 30p 10-bit 4:2:2 w/ no pixel binning', category: 'Electronics', quantity: 1 },
        { id: 2, name: 'Airpods', image: 'https://i.pinimg.com/1200x/08/8d/d4/088dd4215f4d441ebdc79f0517996aa0.jpg', price: 539, description: 'AirPods are compact, Bluetooth-enabled earbuds created by Apple. They are known for easy pairing, lightweight design, and tight integration with the Apple ecosystem. They come with a small charging case that stores and recharges the earbuds when not in use', category: 'Electronics', quantity: 1 },
        { id: 7, name: 'Speakers', image: 'https://i.pinimg.com/736x/5b/81/86/5b8186a7416ba7381a906277d0a978df.jpg', price: 689, description: 'A collection of stills and motion work created for the ID Team at Sonos for the launch of their newly designed and released Roam speaker.', category: 'Electronics', quantity: 1 },
        { id: 8, name: 'Controller', image: 'https://i.pinimg.com/1200x/f2/47/eb/f247ebf102ea110e6a45ae89328176ee.jpg', price: 780, description: 'Photography,Advertising,CGI,Adobe Photoshop,Autodesk 3ds Max, Corona Renderer', category: 'Electonics', quantity: 1 },
      ],


      productsClothes: [

        { id: 3, name: 'Pants', image: 'https://i.pinimg.com/736x/61/8c/06/618c0641b0a01a22be7488d28603f9ea.jpg', price: 150, description: 'To find out about the Manfinity EZcore Men Flap Pocket Side Drawstring Waist Cargo Trousers at SHEIN, part of our latest Men Bottoms ready to shop online today!', category: 'Clothes', quantity: 1 },
        { id: 9, name: 'Long Sleeve', image: 'https://i.pinimg.com/1200x/6a/7f/75/6a7f759dd3eedb7ee6958f204b61596c.jpg', price: 120, description: 'In order to provide you with the best experience, all our products are made by master craftsmen with selected high-quality materials and everyone owns its unique positive meaning.', category: 'Clothes', quantity: 1 },
        { id: 12, name: 'Jacket', image: 'https://i.pinimg.com/1200x/ce/32/02/ce320288c85bb8ae410da272410eb39f.jpg', price: 89, description: 'Crush your workouts in style. Functional activewear from Newsoles. Shop For T-Shirts, Shorts, Jackets, Vests, Sets and Trainers. View Our Activewear Collection Now!', category: 'Clothes', quantity: 1 },
        { id: 10, name: 'Hoodie', image: 'https://i.pinimg.com/1200x/55/f9/09/55f90989f595436126d25600e5b6f1a9.jpg', price: 130, description: 'Over 50 diverse mockup motifs suitable for every situation', category: 'Clothes', quantity: 1 },
      ],

      productAccessories: [
        { id: 4, name: 'Watch', image: 'https://i.pinimg.com/1200x/38/d7/81/38d781e035d252350012cfad10af5498.jpg', price: 935, description: 'Celebrate the last days of summer by shopping our Labor Day Sale. Choose from pieces that seamlessly transition between seasons, like the JX2 Dive Watch. The sale ends soon, so don’t miss your chance!', category: 'Accessories', quantity: 1 },
        { id: 5, name: 'Sunglasses', image: 'https://i.pinimg.com/1200x/e7/e6/6d/e7e66d7ef504ac67d1476dc681193af9.jpg', price: 99, description: 'Choppers Biker Mens Sunglasses - Black C19', category: 'Accessories', quantity: 1 },
        { id: 6, name: 'Boots', image: 'https://i.pinimg.com/1200x/0f/35/78/0f3578d169b85a85df3575b047bd039a.jpg', price: 547, description: 'LEATHER CHELSEA BOOTS', category: 'Accessories', quantity: 1 },
        { id: 11, name: 'Hat', image: 'https://i.pinimg.com/1200x/13/b3/f2/13b3f2c8624daf1479bf631f0b3ed7b1.jpg', price: 70, description: 'Your favorite trucker hat just restocked. FEATURE Spike Trucker Hat is available now at all retail locations + online. Shop Now', category: 'Accessories', quantity: 1 },
      ],








      productdetail: [],
      orderhistory: [],
      addToCart: [],
      currentPage: 'Home',
      Cartmodal: false,
      checkOut: false,
      detailsModal: false,
      total: 0,
      confirmModal: false,
      category: 'all',
      name: '',
      gmail: '',
      addST: '',
      addBT: '',
    }
  },
  methods: {
    navi(i) {
      this.currentPage = i;
    },

    cartModal(modal) {
      this.Cartmodal = modal;
    },

    checkOutModal(modal) {

      this.checkOut = modal;
    },

    cart(index) {
      this.addToCart.push(index);
      this.total += index.price
      if (this.addToCart[index].quantity == 0) {
        this.addToCart[index].quantity += 1;
      } else {

      }
    },

    todetails(detail) {
      this.productdetail.push(detail);

    },

    modalDetails(modal) {
      this.detailsModal = modal;
    },

    minus(i) {
      this.total -= this.addToCart[i].price;
      this.addToCart.splice(i, 1);
    },

    multiplyTotal(i) {
      this.total += this.addToCart[i].price;
      this.addToCart[i].quantity += 1;
    },

    closeCheckOutModal(i) {
      alert('Checkout Successfully')
      this.checkOut = i;
    },

    deTotal(i) {
      if (this.addToCart[i].quantity > 1) {
        this.addToCart[i].quantity -= 1
        this.total -= this.addToCart[i].price;
      } else if (this.addToCart[i].quantity == 1) {
        this.total -= this.addToCart[i].price;
        this.addToCart.splice(i, 1);
      }
    },

    showconfirmmodal(i) {
      this.orderhistory.push(...this.addToCart);
      this.addToCart = [];
      this.confirmModal = i;
    },

    closeCheckOut(i) {
      this.checkOut = i;
    },

    exploreProducts(i) {
      this.currentPage = i;
    },

    changeCategory(c) {
      this.category = c;
    },

    fname(i) {
      this.name = i;
    },
    fgmail(i) {
      this.gmail = i;
    },
    faddS(i) {
      this.addST = i;
    },
    faddB(i) {
      this.addBT = i;
    },

    cartModalI(i){
      this.Cartmodal = i;
    }

  }
}
</script>

<template>
  <Navbar @goTo="navi" @showModalCart="cartModal" :page="currentPage" :cart="addToCart" />
  <Home v-if="currentPage === 'Home'" />
  <FeaturedProducts v-if="currentPage === 'Home'" @explore="exploreProducts" @changeC="changeCategory" @toP="navi" />
  <Products v-if="currentPage === 'Products'" @details="todetails" @modalD="modalDetails"
    :toproducts="productsElectronics" :toproductsClothes="productsClothes" :toproductsAccessories="productAccessories"
    @toCart="cart" :changetoC="category" @changeCP="changeCategory" />
  <CartItem v-if="Cartmodal" @ShowCartModal="cartModal" @showCheckModal="checkOutModal" :toCartItem="addToCart"
    @decreaseTotal="deTotal" :subT="total" @minusan="minus" @multiply="multiplyTotal" />
  <OrderHistory v-if="currentPage === 'OrderHistory'" :toOrderHistory="orderhistory" :subT="total" :toName="name"
    :toGmail="gmail" :toAddST="addST" :toAddBT="addBT" />
  <ProductsDetailsModal :mydetails="productdetail" @detailModal="modalDetails" @toCart="cart" />
  <ConfirmationModal v-if="confirmModal" @toconfirm="showconfirmmodal" />
  <Footer />
  <CheckOutForm v-if="checkOut" @closeCheckOut="checkOutModal" @closeCheckModal="closeCheckOutModal"
    @toconfirm="showconfirmmodal" @closeModal="closeCheckOut" @name="fname" @gmail="fgmail" @addS="faddS"
    @addB="faddB" @ShowCartModal="cartModalI" />

</template>
