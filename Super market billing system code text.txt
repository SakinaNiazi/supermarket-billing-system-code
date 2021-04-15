############################################CREATED BY 2k19/se/107 and 156 #################################
from tkinter import *
import random


class SM_bill:
    def __init__(self, root):
        self.root = root
        self.root.geometry("1300x600+10+5")

        self.root.title("Super Market Billing Software")


        self.root.maxsize(width=1270, height=600)
        self.root.minsize(width=1270, height=700)

        # ====================Variables========================#
        self.cus_name = StringVar()
        self.c_phone = StringVar()
        # For Generating Random Bill Numbers
        x = random.randint(1200, 8999)
        self.c_bill_no = StringVar()
        # Seting Value to variable
        self.c_bill_no.set(str(x))

        self.soap = IntVar()
        self.hand_wash = IntVar()

        self.face_wash = IntVar()
        self.face_primer = IntVar()
        self.body_lotion = IntVar()
        self.rice = IntVar()

        self.fruit = IntVar()

        self.Dried_Beans = IntVar()
        self.vegetables = IntVar()
        self.sugar = IntVar()
        self.pizza = IntVar()
        self.coke = IntVar()

        self.frooti = IntVar()
        self.salt = IntVar()
        self.biscuits = IntVar()
        self.total_cosmetics = StringVar()
        self.total_grocery = StringVar()

        self.total_other = StringVar()
        self.tax_cos = StringVar()

        self.tax_groc = StringVar()
        self.tax_other = StringVar()

        # ===================================
        bg_color = "green"
        fg_color = "black"
        lbl_color = 'black'
        # Title of App
        title = Label(self.root, text="********SUPER MARKET BILLING SOFTWARE**********",
                      bd=12, relief=GROOVE, fg=fg_color, bg=bg_color,

                      font=("times new roman", 30, "bold"), pady=3).pack(fill=X)

        # ==========Customers Frame==========#
        F1 = LabelFrame(text="Customer Details", font=("time new roman",
                                                       12, "bold"), fg="green", bg=bg_color,
                        relief=GROOVE, bd=10)
        F1.place(x=0, y=80, relwidth=1)







        # ===============Customer Name===========#
        cname_lbl = Label(F1, text="Customer Name", bg=bg_color, fg=fg_color,
                          font=("times new roman", 15, "bold")).grid(row=0, column=0, padx=10, pady=5)
        cname_en = Entry(F1, bd=8, relief=GROOVE, textvariable=self.cus_name)
        cname_en.grid(row=0, column=1, ipady=4, ipadx=30, pady=5)

        # =================Customer Phone==============#


        cphon_lbl = Label(F1, text="Mobile No", bg=bg_color, fg=fg_color,
                          font=("times new roman", 15, "bold")).grid(


            row=0, column=2, padx=20)
        cphon_en = Entry(F1, bd=8, relief=GROOVE, textvariable=self.c_phone)
        cphon_en.grid(row=0, column=3, ipady=4, ipadx=30, pady=5)

        # ====================Customer Bill No==================#
        cbill_lbl = Label(F1, text="Bill No.", bg=bg_color, fg=fg_color,
                          font=("times new roman", 15, "bold"))



        cbill_lbl.grid(row=0, column=4, padx=20)
        cbill_en = Entry(F1, bd=8, relief=GROOVE, textvariable=self.c_bill_no)
        cbill_en.grid(row=0, column=5, ipadx=30, ipady=4, pady=5)

        # ====================Bill Search Button===============#
        bill_btn = Button(F1, text="Enter", bd=7, relief=GROOVE,
                          font=("times new roman", 12, "bold"), bg=bg_color,

                          fg=fg_color)
        bill_btn.grid(row=0, column=6, ipady=5, padx=60, ipadx=19, pady=5)

        # ==================Cosmetics Frame=====================#
        F2 = LabelFrame(self.root, text='Cosmetics', bd=10, relief=GROOVE, bg=bg_color, fg="gold",

                        font=("times new roman", 13, "bold"))
        F2.place(x=5, y=180, width=325, height=380)



        # ===========Frame Content
        bath_lbl = Label(F2, font=("times new roman", 15, "bold"), fg=lbl_color,
                         bg=bg_color, text=" Soap")
        bath_lbl.grid(row=0, column=0, padx=10, pady=20)

        bath_en = Entry(F2, bd=8, relief=GROOVE, textvariable=self.soap)
        bath_en.grid(row=0, column=1, ipady=5, ipadx=5)

        # =======Face Cream
        face_lbl = Label(F2, font=("times new roman", 15, "bold"), fg=lbl_color,

                         bg=bg_color, text="Hand wash")
        face_lbl.grid(row=1, column=0, padx=10, pady=20)
        face_en = Entry(F2, bd=8, relief=GROOVE, textvariable=self.hand_wash)
        face_en.grid(row=1, column=1, ipady=5, ipadx=5)

        # ========Face Wash
        wash_lbl = Label(F2, font=("times new roman", 15, "bold"),

                         fg=lbl_color, bg=bg_color, text="Face wash")
        wash_lbl.grid(row=2, column=0, padx=10, pady=20)

        wash_en = Entry(F2, bd=8, relief=GROOVE, textvariable=self.face_wash)
        wash_en.grid(row=2, column=1, ipady=5, ipadx=5)

        # ========Hair Spray
        hair_lbl = Label(F2, font=("times new roman", 15, "bold"),
                         fg=lbl_color, bg=bg_color, text="face primer")

        hair_lbl.grid(row=3, column=0, padx=10, pady=20)
        hair_en = Entry(F2, bd=8, relief=GROOVE, textvariable=self.face_primer)

        hair_en.grid(row=3, column=1, ipady=5, ipadx=5)

        # ============Body Lotion
        lot_lbl = Label(F2, font=("times new roman", 15, "bold"),
                        fg=lbl_color, bg=bg_color, text="Body Lotion")
        lot_lbl.grid(row=4, column=0, padx=10, pady=20)
        lot_en = Entry(F2, bd=8, relief=GROOVE, textvariable=self.body_lotion)
        lot_en.grid(row=4, column=1, ipady=5, ipadx=5)

        # ==================Grocery Frame=====================#

        F2 = LabelFrame(self.root, text='Grocery', bd=10, relief=GROOVE, bg=bg_color, fg="gold",
                        font=("times new roman", 13, "bold"))

        F2.place(x=330, y=180, width=325, height=380)

        # ===========Frame Content
        rice_lbl = Label(F2, font=("times new roman", 15, "bold"),
                         fg=lbl_color, bg=bg_color, text="Rice")
        rice_lbl.grid(row=0, column=0, padx=10, pady=20)

        rice_en = Entry(F2, bd=8, relief=GROOVE, textvariable=self.rice)
        rice_en.grid(row=0, column=1, ipady=5, ipadx=5)

        # =======
        oil_lbl = Label(F2, font=("times new roman", 15, "bold"),
                        fg=lbl_color, bg=bg_color, text="Dried Beans")
        oil_lbl.grid(row=1, column=0, padx=10, pady=20)

        oil_en = Entry(F2, bd=8, relief=GROOVE, textvariable=self.Dried_Beans)
        oil_en.grid(row=1, column=1, ipady=5, ipadx=5)

        # =======
        daal_lbl = Label(F2, font=("times new roman", 15, "bold"),

                         fg=lbl_color, bg=bg_color, text="fruit")
        daal_lbl.grid(row=2, column=0, padx=10, pady=20)

        daal_en = Entry(F2, bd=8, relief=GROOVE, textvariable=self.fruit)
        daal_en.grid(row=2, column=1, ipady=5, ipadx=5)

        # ========
        wheat_lbl = Label(F2, font=("times new roman", 15, "bold"),

                          fg=lbl_color, bg=bg_color, text="vegetables")
        wheat_lbl.grid(row=3, column=0, padx=10, pady=20)
        wheat_en = Entry(F2, bd=8, relief=GROOVE, textvariable=self.vegetables)
        wheat_en.grid(row=3, column=1, ipady=5, ipadx=5)

        # ============
        sugar_lbl = Label(F2, font=("times new roman", 15, "bold"),
                          fg=lbl_color, bg=bg_color, text="Sugar")

        sugar_lbl.grid(row=4, column=0, padx=10, pady=20)
        sugar_en = Entry(F2, bd=8, relief=GROOVE, textvariable=self.sugar)
        sugar_en.grid(row=4, column=1, ipady=5, ipadx=5)

        # ==================Other Stuff=====================#

        F2 = LabelFrame(self.root, text='more products', bd=10, relief=GROOVE, bg=bg_color, fg="gold",
                        font=("times new roman", 13, "bold"))

        F2.place(x=655, y=180, width=325, height=380)



        # ===========Frame Content
        maza_lbl = Label(F2, font=("times new roman", 15, "bold"),

                         fg=lbl_color, bg=bg_color, text="pizza")
        maza_lbl.grid(row=0, column=0, padx=10, pady=20)

        maza_en = Entry(F2, bd=8, relief=GROOVE, textvariable=self.pizza)
        maza_en.grid(row=0, column=1, ipady=5, ipadx=5)

        # =======
        cock_lbl = Label(F2, font=("times new roman", 15, "bold"),
                         fg=lbl_color, bg=bg_color, text="Coke")
        cock_lbl.grid(row=1, column=0, padx=10, pady=20)
        cock_en = Entry(F2, bd=8, relief=GROOVE, textvariable=self.coke)
        cock_en.grid(row=1, column=1, ipady=5, ipadx=5)

        # =======
        frooti_lbl = Label(F2, font=("times new roman", 15, "bold"),
                           fg=lbl_color, bg=bg_color, text="Frooti")


        frooti_lbl.grid(row=2, column=0, padx=10, pady=20)
        frooti_en = Entry(F2, bd=8, relief=GROOVE, textvariable=self.frooti)

        frooti_en.grid(row=2, column=1, ipady=5, ipadx=5)

        # ========
        cold_lbl = Label(F2, font=("times new roman", 15, "bold"),

                         fg=lbl_color, bg=bg_color, text="salt")

        cold_lbl.grid(row=3, column=0, padx=10, pady=20)
        cold_en = Entry(F2, bd=8, relief=GROOVE, textvariable=self.salt)
        cold_en.grid(row=3, column=1, ipady=5, ipadx=5)

        # ============



        bis_lbl = Label(F2, font=("times new roman", 15, "bold"),
                        fg=lbl_color, bg=bg_color, text="Biscuits")
        bis_lbl.grid(row=4, column=0, padx=10, pady=20)

        bis_en = Entry(F2, bd=8, relief=GROOVE, textvariable=self.biscuits)
        bis_en.grid(row=4, column=1, ipady=5, ipadx=5)

        # ===================Bill Aera================#
        F3 = Label(self.root, bd=10, relief=GROOVE)

        F3.place(x=960, y=180, width=325, height=380)
        # ===========


        bill_title = Label(F3, text="SUPERMARKET BILL ", font=("Lucida", 13, "bold"), bd=7, relief=GROOVE)
        bill_title.pack(fill=X)

        # ============
        scroll_y = Scrollbar(F3, orient=VERTICAL)
        self.txt = Text(F3, yscrollcommand=scroll_y.set)
        scroll_y.pack(side=RIGHT, fill=Y)
        scroll_y.config(command=self.txt.yview)
        self.txt.pack(fill=BOTH, expand=1)


        # ===========Buttons Frame=============#
        F4 = LabelFrame(self.root, text='Bill Menu', bd=10, relief=GROOVE, bg=bg_color, fg="gold",
                        font=("times new roman", 13, "bold"))


        F4.place(x=0, y=560, relwidth=1, height=145)

        # ===================
        cosm_lbl = Label(F4, font=("times new roman", 15, "bold"),
                         fg=lbl_color, bg=bg_color, text="Total Cosmetics")

        cosm_lbl.grid(row=0, column=0, padx=10, pady=0)

        cosm_en = Entry(F4, bd=8, relief=GROOVE, textvariable=self.total_cosmetics)

        cosm_en.grid(row=0, column=1, ipady=2, ipadx=5)

        # ===================

        gro_lbl = Label(F4, font=("times new roman", 15, "bold"),
                        fg=lbl_color, bg=bg_color, text="Total Grocery")
        gro_lbl.grid(row=1, column=0, padx=10, pady=5)
        gro_en = Entry(F4, bd=8, relief=GROOVE, textvariable=self.total_grocery)
        gro_en.grid(row=1, column=1, ipady=2, ipadx=5)



        # ================

        oth_lbl = Label(F4, font=("times new roman", 15, "bold"),

                        fg=lbl_color, bg=bg_color, text="Others Total")
        oth_lbl.grid(row=2, column=0, padx=10, pady=5)

        oth_en = Entry(F4, bd=8, relief=GROOVE, textvariable=self.total_other)
        oth_en.grid(row=2, column=1, ipady=2, ipadx=5)

        # ================
        cosmt_lbl = Label(F4, font=("times new roman", 15, "bold"), fg=lbl_color,

                          bg=bg_color, text="Cosmetics Tax")
        cosmt_lbl.grid(row=0, column=2, padx=30, pady=0)

        cosmt_en = Entry(F4, bd=8, relief=GROOVE, textvariable=self.tax_cos)

        cosmt_en.grid(row=0, column=3, ipady=2, ipadx=5)

        # =================
        grot_lbl = Label(F4, font=("times new roman", 15, "bold"), fg=lbl_color,
                         bg=bg_color, text="Grocery Tax")


        grot_lbl.grid(row=1, column=2, padx=30, pady=5)
        grot_en = Entry(F4, bd=8, relief=GROOVE, textvariable=self.tax_groc)

        grot_en.grid(row=1, column=3, ipady=2, ipadx=5)

        # ==================
        otht_lbl = Label(F4, font=("times new roman", 15, "bold"),

                         fg=lbl_color, bg=bg_color, text="Others Tax")

        otht_lbl.grid(row=2, column=2, padx=10, pady=5)

        otht_en = Entry(F4, bd=8, relief=GROOVE, textvariable=self.tax_other)
        otht_en.grid(row=2, column=3, ipady=2, ipadx=5)



        # ====================
        total_btn = Button(F4, text="Total", bg=bg_color, fg=fg_color,
                           font=("lucida", 12, "bold"), bd=7, relief=GROOVE,
                           command=self.total)

        total_btn.grid(row=1, column=4, ipadx=20, padx=30)

        # ========================
        genbill_btn = Button(F4, text="Generate Bill", bg=bg_color, fg=fg_color,
                             font=("lucida", 12, "bold"), bd=7,

                             relief=GROOVE, command=self.bill_area)
        genbill_btn.grid(row=1, column=5, ipadx=20)

        # ====================
        clear_btn = Button(F4, text="Clear", bg=bg_color, fg=fg_color,

                           font=("lucida", 12, "bold"), bd=7, relief=GROOVE,
                           command=self.clear)

        clear_btn.grid(row=1, column=6, ipadx=20, padx=30)

        # ======================
        exit_btn = Button(F4, text="Exit", bg=bg_color, fg=fg_color,
                          font=("lucida", 12, "bold"), bd=7, relief=GROOVE,
                          command=self.exit)
        exit_btn.grid(row=1, column=7, ipadx=20)



    # Function to get total prices
    def total(self):
        # =================Total Cosmetics Prices
        self.total_cosmetics_prices = (
                (self.soap.get() * 40) +
                (self.hand_wash.get() * 140) +
                (self.face_wash.get() * 240) +
                (self.face_primer.get() * 340) +
                (self.body_lotion.get() * 260)
        )
        self.total_cosmetics.set("Rs. " + str(self.total_cosmetics_prices))

        self.tax_cos.set("Rs. " + str(round(self.total_cosmetics_prices * 0.05)))
        # ====================Total Grocery Prices

        self.total_grocery_prices = (

                (self.rice.get() * 100) +
                (self.Dried_Beans.get() * 180) +
                (self.fruit.get() * 80) +
                (self.vegetables.get() * 80) +
                (self.sugar.get() * 170)

        )


        self.total_grocery.set("Rs. " + str(self.total_grocery_prices))


        self.tax_groc.set("Rs. " + str(round(self.total_grocery_prices * 0.05)))
        # ======================Total Other Prices

        self.total_other_prices = (
                (self.pizza.get() * 20) +
                (self.frooti.get() * 50) +
                (self.coke.get() * 60) +
                (self.salt.get() * 20) +
                (self.biscuits.get() * 20)
        )
        self.total_other.set("Rs. " + str(self.total_other_prices))
        self.tax_other.set("Rs. " + str(round(self.total_other_prices * 0.05)))

    # Function For Text Area
    def welcome_soft(self):
        self.txt.delete('1.0', END)
        self.txt.insert(END, "       Welcome To Hanan's Retail\n")
        self.txt.insert(END, f"\nBill No. : {str(self.c_bill_no.get())}")



        self.txt.insert(END, f"\nCustomer Name : {str(self.cus_name.get())}")
        self.txt.insert(END, f"\nPhone No. : {str(self.c_phone.get())}")
        self.txt.insert(END, "\n===================================")
        self.txt.insert(END, "\nProduct          Qty         Price")
        self.txt.insert(END, "\n===================================")

    # Function to clear the bill area
    def clear(self):
        self.txt.delete('1.0', END)

    # Add Product name , qty and price to bill area
    def bill_area(self):
        self.welcome_soft()
        if self.soap.get() != 0:
            self.txt.insert(END, f"\n Soap         {self.soap.get()}      "
                                 f"     {self.soap.get() * 40}")
        if self.hand_wash.get() != 0:
            self.txt.insert(END, f"\n hand wash        "
                                 f"{self.hand_wash.get()}         "
                                 f"  {self.hand_wash.get() * 140}")
        if self.face_wash.get() != 0:
            self.txt.insert(END, f"\nFace Wash         {self.face_wash.get()}  "
                                 f"    {self.face_wash.get() * 240}")
        if self.face_wash.get() != 0:
            self.txt.insert(END, f"\nface wash        {self.face_wash.get()}   "
                                 f"        {self.face_wash.get() * 340}")
        if self.body_lotion.get() != 0:
            self.txt.insert(END,
                            f"\nBody Lotion       {self.body_lotion.get()}      "
                            f"     {self.body_lotion.get() * 260}")
        if self.face_primer.get() != 0:
            self.txt.insert(END, f"\nWheat             {self.face_primer.get()}     "
                                 f"      {self.face_primer.get() * 100}")
        if self.vegetables.get() != 0:
            self.txt.insert(END, f"\nFood Oil          {self.vegetables.get()}        "
                                 f"   {self.vegetables.get() * 180}")
        if self.fruit.get() != 0:
            self.txt.insert(END, f"\nFruit              {self.fruit.get()}     "
                                 f"      {self.fruit.get() * 80}")
        if self.rice.get() != 0:
            self.txt.insert(END, f"\nRice              {self.rice.get()}       "
                                 f"    {self.rice.get() * 80}")
        if self.sugar.get() != 0:
            self.txt.insert(END, f"\nSugar             {self.sugar.get()}       "
                                 f"    {self.sugar.get() * 170}")
        if self.pizza.get() != 0:
            self.txt.insert(END, f"\nPizza              {self.pizza.get()}     "
                                 f"      {self.pizza.get() * 20}")
        if self.frooti.get() != 0:
            self.txt.insert(END, f"\nFrooti            {self.frooti.get()}    "
                                 
                                 
                                 f"       {self.frooti.get() * 50}")
        if self.coke.get() != 0:
            self.txt.insert(END, f"\nCoke              {self.coke.get()}      "
                                 
                                 
                                 f"     {self.coke.get() * 60}")
        if self.salt.get() != 0:
            self.txt.insert(END, f"\nSalt             {self.salt.get()}        "
                                 f"   {self.salt.get() * 20}")
        if self.biscuits.get() != 0:
            self.txt.insert(END, f"\nBiscuits          {self.biscuits.get()}         "
                                 f"  {self.biscuits.get() * 20}")
        self.txt.insert(END, "\n===================================")
        self.txt.insert(END,
                        f"\n                   "
                        f"   Total : {self.total_cosmetics_prices + self.total_grocery_prices + self.total_other_prices + self.total_cosmetics_prices * 0.05 + self.total_grocery_prices * 0.05 + self.total_other_prices * 0.05}")

    # Function to exit

    def exit(self):

        self.root.destroy()

    # Function To Clear All Fields


root = Tk()
object = SM_bill(root)
root.mainloop()



