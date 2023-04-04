# Workshop-Cost-Calculator
Calculates the cost of a workshop based on days and travel costs. 

//Benjamin Glass 
//Intro to computer program assignment 3
//Program lets people prepare for their workshops with the costs. 
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;
using System.Xml;

namespace Benjamin_Glass_assignment_3
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }
        private void listBox1_SelectedIndexChanged(object sender, EventArgs e)
        {

        }

        private void label1_Click(object sender, EventArgs e)
        {

        }

        private void Form1_Load(object sender, EventArgs e)
        {

        }

        private void button1_Click(object sender, EventArgs e)
        {
            //Each variable represents an array for the values for the representative groups: days for days of each workshop, location fees, etc. 
            int[] days = new int[5] {
                3, 3, 3, 5, 1
            };
            int[] regFees = new int[5] {
                1000, 800, 1500, 1300, 500
            };
            int[] locationFees = new int[6] {
                150, 225, 175, 300, 175, 150
            };
            int price = (days[listBox1.SelectedIndex] * locationFees[listBox2.SelectedIndex]) + regFees[listBox1.SelectedIndex];
            listBox3.Items.Clear();
            listBox3.Items.Add("Regristration Fees: $" + regFees[listBox1.SelectedIndex].ToString());
            listBox3.Items.Add("Lodging Fees: $" + (days[listBox1.SelectedIndex] * locationFees[listBox2.SelectedIndex]).ToString());
            listBox3.Items.Add("Total Cost:");
            listBox3.Items.Add("$" + price.ToString())
            switch (price)
            {
                case > 1500:
                    listBox3.Items.Add("Wow that's a lot!");
                    break;
                case default:
                    break;
            }

        }
    }
}
