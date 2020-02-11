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


    
    public partial class Form1 : Form
    {
       

        public void SetFromForm2()
        {
            BtnPretraga_Click(null, null);
        }
        private bool mBool;
        public Form1()
        {
            InitializeComponent();
        }

        public Form1(bool iniciajalizujGrid)
        {
            InitializeComponent();
            mBool = iniciajalizujGrid;
            
            label1.Text = "Grid";
            label2.Text = "Proba";

           
        }

     
        private void Button1_Click(object sender, EventArgs e)
        {
            Form2 frm = new Form2();
            frm.AdviseParent += new Form2.AdviseParentEventHandler(SetFromForm2);

            frm.ShowDialog();

           
          
           






        }

        private void Form1_Load(object sender, EventArgs e)
        {
            if(mBool )
            {

                label1.Text = "Grid";
            }
        }

        private void BtnPretraga_Click(object sender, EventArgs e)
        {
            label1.Text = "Osvezenje";
        }
    }
}
