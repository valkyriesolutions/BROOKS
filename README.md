Public Class Form1

    Private Sub Form1_Load(sender As Object, e As EventArgs) Handles MyBase.Load
        Timer1.Start()
        Timer1.Interval = 20000

        Panel2.BackColor = Color.Red
    End Sub

    Private Sub Timer1_Tick(sender As Object, e As EventArgs) Handles Timer1.Tick
        If Timer1.Interval = 20000 Then

            Timer1.Stop()
            Panel2.BackColor = Color.Black

            Timer2.Start()
            Timer2.Interval = 10000
            Panel3.BackColor = Color.Yellow

        End If
    End Sub

    Private Sub Timer2_Tick(sender As Object, e As EventArgs) Handles Timer2.Tick
        If Timer2.Interval = 10000 Then

            Timer2.Stop()
            Panel3.BackColor = Color.Black

            Timer3.Start()
            Timer3.Interval = 20000
            Panel4.BackColor = Color.Green

        End If

    End Sub

    Private Sub Timer3_Tick(sender As Object, e As EventArgs) Handles Timer3.Tick
        If Timer3.Interval = 20000 Then

            Timer3.Stop()
            Panel4.BackColor = Color.Black

        End If

        Timer1.Start()
        Timer1.Interval = 20000

        Panel2.BackColor = Color.Red
    End Sub
End Class
