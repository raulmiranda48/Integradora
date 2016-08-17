
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;
using System.IO.Ports;
using ComunicacionArduino.Properties;
namespace ComunicacionArduino
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
            serialPort1.PortName = "COM3";
            serialPort1.BaudRate = 9600;
       
        }

        private void form1_formClosing(Object sender, FormClosedEventArgs e)
        {
            if (serialPort1.IsOpen) serialPort1.Close();
        }
