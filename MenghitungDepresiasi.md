# Source Code Form 

/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package praktik;

/**
 *
 * @author legion
 */
import java.sql.Connection;

import java.sql.PreparedStatement;

import java.sql.ResultSet;

import java.sql.SQLException;

import java.sql.Statement;

import javax.swing.JOptionPane;

import javax.swing.table.DefaultTableModel;

public class Formisi extends javax.swing.JFrame {

    /**
     * Creates new form Formisi
     */
    
    private int HP, NR, UE, HASIL;
    
    public Formisi() {
        
        initComponents();
    }

    /**
     
     * This method is called from within the constructor to initialize the form.
     
     * WARNING: Do NOT modify this code. The content of this method is always
     
     * regenerated by the Form Editor.
     */
    
    @SuppressWarnings("unchecked")
    
    // <editor-fold defaultstate="collapsed" desc="Generated Code">                          
    
    private void initComponents() {

        jLabel1 = new javax.swing.JLabel();
        
        jLabel2 = new javax.swing.JLabel();
        
        jLabel3 = new javax.swing.JLabel();
        
        TX_HP = new javax.swing.JTextField();
        
        TX_NR = new javax.swing.JTextField();
        
        TX_UE = new javax.swing.JTextField();
        
        TX_HASIL = new javax.swing.JTextField();
        
        BT_SIMPAN = new javax.swing.JButton();
        
        BT_HASIL = new javax.swing.JButton();
        
        jLabel4 = new javax.swing.JLabel();
        
        jLabel5 = new javax.swing.JLabel();
        
        jLabel6 = new javax.swing.JLabel();
        
        jLabel7 = new javax.swing.JLabel();
        
        BT_OUT = new javax.swing.JButton();

        setDefaultCloseOperation(javax.swing.WindowConstants.EXIT_ON_CLOSE);

        jLabel1.setFont(new java.awt.Font("Times New Roman", 0, 14)); // NOI18N
        
        jLabel1.setText("Harga Perolehan");

        jLabel2.setFont(new java.awt.Font("Times New Roman", 0, 14)); // NOI18N
        
        jLabel2.setText("Nilai Residu");

        jLabel3.setFont(new java.awt.Font("Times New Roman", 0, 14)); // NOI18N
        
        jLabel3.setText("Umur Ekonomis");

        TX_HP.setFont(new java.awt.Font("Times New Roman", 0, 14)); // NOI18N

        TX_NR.setFont(new java.awt.Font("Times New Roman", 0, 14)); // NOI18N

        TX_UE.setFont(new java.awt.Font("Times New Roman", 0, 14)); // NOI18N

        TX_HASIL.setFont(new java.awt.Font("Times New Roman", 0, 14)); // NOI18N
        
        TX_HASIL.addActionListener(new java.awt.event.ActionListener() {
            
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                
                TX_HASILActionPerformed(evt);
            }
        });

        BT_SIMPAN.setFont(new java.awt.Font("Times New Roman", 0, 14)); // NOI18N
        
        BT_SIMPAN.setText("SIMPAN");
        
        BT_SIMPAN.addActionListener(new java.awt.event.ActionListener() {
            
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                
                BT_SIMPANActionPerformed(evt);
            }
        });

        BT_HASIL.setFont(new java.awt.Font("Times New Roman", 0, 14)); // NOI18N
        
        BT_HASIL.setText("HASIL");
        
        BT_HASIL.addActionListener(new java.awt.event.ActionListener() {
            
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                
                BT_HASILActionPerformed(evt);
            }
        });

        jLabel4.setFont(new java.awt.Font("Times New Roman", 0, 24)); // NOI18N
        
        jLabel4.setText("Menghitung Depresiasi");

        jLabel5.setFont(new java.awt.Font("Times New Roman", 0, 14)); // NOI18N
        
        jLabel5.setText("TAHUN");

        jLabel6.setText("Rp");

        jLabel7.setText("Rp");

        BT_OUT.setFont(new java.awt.Font("Times New Roman", 0, 14)); // NOI18N
        
        BT_OUT.setText("KELUAR");
        
        BT_OUT.addActionListener(new java.awt.event.ActionListener() {
            
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                
                BT_OUTActionPerformed(evt);
            }
        });

        javax.swing.GroupLayout layout = new javax.swing.GroupLayout(getContentPane());
        
        getContentPane().setLayout(layout);
        
        layout.setHorizontalGroup(
            
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            
            .addGroup(layout.createSequentialGroup()
                
                .addContainerGap()
                
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    
                    .addGroup(layout.createSequentialGroup()
                        
                        .addComponent(BT_SIMPAN)
                        
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.UNRELATED)
                        
                        .addComponent(BT_OUT))
                    
                    .addGroup(layout.createSequentialGroup()
                        
                        .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.TRAILING)
                            
                            .addGroup(layout.createSequentialGroup()
                                
                                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.TRAILING)
                                    
                                    .addComponent(jLabel2, javax.swing.GroupLayout.Alignment.LEADING)
                                    
                                    .addComponent(jLabel3, javax.swing.GroupLayout.Alignment.LEADING))
                                
                                .addGap(36, 36, 36))
                            
                            .addComponent(BT_HASIL))
                        
                        .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                            
                            .addGroup(layout.createSequentialGroup()
                                
                                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                                
                                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                                    
                                    .addGroup(layout.createSequentialGroup()
                                        
                                        .addComponent(TX_UE, javax.swing.GroupLayout.PREFERRED_SIZE, 35, javax.swing.GroupLayout.PREFERRED_SIZE)
                                        
                                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                                        
                                        .addComponent(jLabel5))
                                    
                                    .addComponent(TX_HASIL, javax.swing.GroupLayout.PREFERRED_SIZE, 92, javax.swing.GroupLayout.PREFERRED_SIZE)))
                            
                            .addGroup(layout.createSequentialGroup()
                                
                                .addGap(5, 5, 5)
                                
                                .addComponent(TX_NR, javax.swing.GroupLayout.PREFERRED_SIZE, 102, javax.swing.GroupLayout.PREFERRED_SIZE))))
                    
                    .addGroup(layout.createSequentialGroup()
                        
                        .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.TRAILING)
                            
                            .addComponent(jLabel7)
                            
                            .addGroup(layout.createSequentialGroup()
                                
                                .addComponent(jLabel1, javax.swing.GroupLayout.PREFERRED_SIZE, 106, javax.swing.GroupLayout.PREFERRED_SIZE)
                                
                                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                                
                                .addComponent(jLabel6)))
                        
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                        
                        .addComponent(TX_HP, javax.swing.GroupLayout.PREFERRED_SIZE, 102, javax.swing.GroupLayout.PREFERRED_SIZE))
                    
                    .addGroup(layout.createSequentialGroup()
                        
                        .addGap(113, 113, 113)
                        
                        .addComponent(jLabel4)))
                
                .addContainerGap(128, Short.MAX_VALUE))
        
        );
        
        layout.setVerticalGroup(
            
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            
            .addGroup(layout.createSequentialGroup()
                
                .addComponent(jLabel4)
                
                .addGap(23, 23, 23)
                
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    
                    .addComponent(jLabel1)
                    
                    .addComponent(TX_HP, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                    
                    .addComponent(jLabel6))
                
                .addGap(18, 18, 18)
                
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    
                    .addComponent(jLabel2)
                    
                    .addComponent(TX_NR, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                    
                    .addComponent(jLabel7))
                
                .addGap(18, 18, 18)
                
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    
                    .addComponent(jLabel3)
                    
                    .addComponent(TX_UE, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                    
                    .addComponent(jLabel5))
                
                .addGap(18, 18, 18)
                
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    
                    .addComponent(TX_HASIL, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                    
                    .addComponent(BT_HASIL))
                
                .addGap(25, 25, 25)
                
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    
                    .addComponent(BT_SIMPAN)
                    
                    .addComponent(BT_OUT))
                
                .addContainerGap(71, Short.MAX_VALUE))
        
        );

        pack();
        
        setLocationRelativeTo(null);
    }
    
    // </editor-fold>                        

    private void BT_SIMPANActionPerformed(java.awt.event.ActionEvent evt) {                                          
        
        // TODO add your handling code here:
        
        //menyederhanakan field
        
        HP = Integer.parseInt(TX_HP.getText());
        
        NR = Integer.parseInt(TX_NR.getText());
        
        UE = Integer.parseInt(TX_UE.getText());
        
        HASIL = Integer.parseInt(TX_HASIL.getText());
        
        try{
            
            Connection conn = koneksi.getkoneksi();
            
            String sql ="INSERT INTO tabel_hasil VALUES('','"+HP+"','"+NR+"','"+UE+"','"+HASIL+"')";
            
            PreparedStatement p = conn.prepareStatement(sql);
            
            JOptionPane.showMessageDialog(null, "Data sudah masuk ke DB!!");
            
            p.executeUpdate();
            
            p.close();
        }
        
        catch (SQLException e){
            
            System.out.println("Error Masukan Data" + e.getMessage());
        }
        
    }                                         

    private void TX_HASILActionPerformed(java.awt.event.ActionEvent evt) {                                         
        
        // TODO add your handling code here:
    }                                        

    private void BT_HASILActionPerformed(java.awt.event.ActionEvent evt) {                                         
        
        // TODO add your handling code here:
        
        int Hasil = 0;
        
        HP = Integer.parseInt(TX_HP.getText());
        
        NR = Integer.parseInt(TX_NR.getText());
        
        UE = Integer.parseInt(TX_UE.getText());
        
        //method perkalian
        
        Hasil = (HP - NR)/UE;
        
        TX_HASIL.setText(""+Hasil);
    }                                        

    private void BT_OUTActionPerformed(java.awt.event.ActionEvent evt) {                                       
        
        // TODO add your handling code here:
        
        dispose();
    }                                      

    /**
     
     * @param args the command line arguments
     
     */
    
    public static void main(String args[]) {
        
        /* Set the Nimbus look and feel */
        
        //<editor-fold defaultstate="collapsed" desc=" Look and feel setting code (optional) ">
        
        /* If Nimbus (introduced in Java SE 6) is not available, stay with the default look and feel.
        
        * For details see http://download.oracle.com/javase/tutorial/uiswing/lookandfeel/plaf.html 
        
        */
        
        try {
            
            for (javax.swing.UIManager.LookAndFeelInfo info : javax.swing.UIManager.getInstalledLookAndFeels()) {
                
                if ("Nimbus".equals(info.getName())) {
                    
                    javax.swing.UIManager.setLookAndFeel(info.getClassName());
                    
                    break;
                }
            }
        } catch (ClassNotFoundException ex) {
            
            java.util.logging.Logger.getLogger(Formisi.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        
        } catch (InstantiationException ex) {
            
            java.util.logging.Logger.getLogger(Formisi.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        
        } catch (IllegalAccessException ex) {
            
            java.util.logging.Logger.getLogger(Formisi.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        
        } catch (javax.swing.UnsupportedLookAndFeelException ex) {
            
            java.util.logging.Logger.getLogger(Formisi.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        }
        
        //</editor-fold>

        /* Create and display the form */
        
        java.awt.EventQueue.invokeLater(new Runnable() {
            
            public void run() {
                
                new Formisi().setVisible(true);
            }
        });
    }

    // Variables declaration - do not modify                     
    
    private javax.swing.JButton BT_HASIL;
    
    private javax.swing.JButton BT_OUT;
    
    private javax.swing.JButton BT_SIMPAN;
    
    private javax.swing.JTextField TX_HASIL;
    
    private javax.swing.JTextField TX_HP;
    
    private javax.swing.JTextField TX_NR;
    
    private javax.swing.JTextField TX_UE;
    
    private javax.swing.JLabel jLabel1;
    
    private javax.swing.JLabel jLabel2;
    
    private javax.swing.JLabel jLabel3;
    
    private javax.swing.JLabel jLabel4;
    
    private javax.swing.JLabel jLabel5;
    
    private javax.swing.JLabel jLabel6;
    
    private javax.swing.JLabel jLabel7;
    
    // End of variables declaration                   
}

