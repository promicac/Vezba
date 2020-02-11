using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;
using BO;

namespace CMS
{

   
    public partial class Form2 : Form
    {
        public delegate void AdviseParentEventHandler();
        public event AdviseParentEventHandler AdviseParent;


        public TipForme mTipForme;
        public Form2()
        {
            InitializeComponent();
        }

        public Form2(BO.TipForme tipForme, string str)
        {
            mTipForme = tipForme;

            Text = str;
            InitializeComponent();
        }

        private void Form2_Load(object sender, EventArgs e)
        {


            if (mTipForme == TipForme.Detalji)
            {
                button1.Text = "Detalji karusela";
            }
            else if (mTipForme == TipForme.Izmena)
            {
                button1.Text = "Izmena karusela";
            }



        }

        private void Form2_FormClosed(object sender, FormClosedEventArgs e)
        {

           


        }

      

        private void Button1_Click(object sender, EventArgs e)
        {
            Close();
            DialogResult = DialogResult.Cancel;
        }

        private void Button2_Click(object sender, EventArgs e)
        {
            Close();
            DialogResult = DialogResult.OK;
           
           

            
        }

        private void Button3_Click(object sender, EventArgs e)
        {


            SetLabelOnForm1();




        }

        private void Button4_Click(object sender, EventArgs e)
        {
          
            DialogResult = DialogResult.OK;

        }

        private void Form2_FormClosing(object sender, FormClosingEventArgs e)
        {
           
        }

        public void SetLabelOnForm1()
        {
            if (AdviseParent != null)
                AdviseParent();
        }
    }
}

