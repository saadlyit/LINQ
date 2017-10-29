using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Data;
using System.Windows.Documents;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Imaging;
using System.Windows.Navigation;
using System.Windows.Shapes;

namespace LINQ
{
    /// <summary>
    /// Interaction logic for MainWindow.xaml
    /// </summary>
    public partial class MainWindow : Window
    {
        public MainWindow()
        {
            InitializeComponent();
        }

        private void bttnadd_Click(object sender, RoutedEventArgs e)
        {
            int[] add = new int[5] { 1,2,3,4,5 };
            listBox.Items.Add("Array ITEMS: 12345");
            listBox.Items.Add("==================");
            int sumtotal = add.Sum();
            listBox.Items.Add(sumtotal);

        }

        private void btnmin_Click(object sender, RoutedEventArgs e)
        {
            int[] add = new int[5] { 1, 2, 3, 4, 5 };
            int minimum = add.Min();
            listBox.Items.Add("The minimum number is: " + minimum);
        }

        private void button_Click(object sender, RoutedEventArgs e)
        {
            int[] add = new int[5] { 1, 2, 3, 4, 5 };
            int maximum = add.Max();
            listBox.Items.Add("The minimum number is: " + maximum);
        }

        private void btncontain_Click(object sender, RoutedEventArgs e)
        {
            int[] add = new int[5] { 1, 2, 3, 4, 5 };
            bool numberconttain = add.Contains(3);
            listBox.Items.Add("The Number it is containing is :" + numberconttain);
        }

        private void btnelemt_Click(object sender, RoutedEventArgs e)
        {
            int[] add = new int[5] { 1, 2, 3, 4, 5 };
            int elemnt = add.ElementAt(2);
            listBox.Items.Add("the itme is located at :" + elemnt);
        }

        private void btndistinc_Click(object sender, RoutedEventArgs e)
        {
            int[] distinc = new int[8] {1,1,2,3,3,4,5,5};
            var dublicatenumbers = distinc.Distinct();
            foreach (var num in dublicatenumbers)
            {
                listBox.Items.Add(num.ToString());
            }

        }

        private void Btnlottery_Click(object sender, RoutedEventArgs e)
        {
            int[] lotnumbers = new int[10] { 43, 31, 7, 22, 29, 16, 10, 4, 7, 41 };
            int[] chosen = new int[6] {31, 9, 8, 43, 22, 1 };
            var take = lotnumbers.Take(6);
            foreach (var num in take)
            {
                listBox.Items.Add(num.ToString());
            }
            var mynumber = chosen.Intersect(take);
            foreach (var sum in mynumber)
            {
                listBox.Items.Add(sum.ToString());
            }
        }
    }
}
